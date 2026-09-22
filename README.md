# Timetable to Calendar

Convert timetable images into structured data and iCalendar (`.ics`) events using OCR.

## Features

- OCR-based timetable extraction
- Table and column detection with OpenCV
- Text recognition with Tesseract OCR
- Timetable parsing with Pandas
- iCalendar generation
- Configurable timezone
- Command-line interface
- Automated tests and GitHub Actions CI

## Requirements

- Python 3.10+
- Tesseract OCR installed and available on your PATH

## Installation

```bash
git clone https://github.com/OrgSagarGupta/Schedule-time-table.git
cd Schedule-time-table
python -m venv .venv
```

Activate the environment and install:

```bash
pip install -e .
pip install pytest
```

## Usage

```bash
timetable path/to/timetable.png --output schedule.ics --timezone Asia/Kolkata
```

Or:

```bash
python -m timetable_converter.cli path/to/timetable.png
```

## Pipeline

```text
Timetable Image
      |
      v
OpenCV preprocessing
      |
      v
Table detection
      |
      v
Tesseract OCR
      |
      v
Column clustering
      |
      v
Pandas timetable
      |
      v
iCalendar (.ics)
```

## Testing

```bash
pytest
```

## Limitations

OCR quality depends on image resolution, table layout, font, and image noise.
The current parser is optimized for timetable layouts similar to the project's example inputs.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT
