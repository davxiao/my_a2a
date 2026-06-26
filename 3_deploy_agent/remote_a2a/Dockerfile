FROM python:3.14-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY remote_time_agent ./remote_time_agent

# Expose the port the app runs on
# this port must be the same in agent.py
EXPOSE 8001

# Set the entrypoint command
CMD ["python", "remote_time_agent/agent.py"]
