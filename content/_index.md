+++
title = "Brendan Ferris"
description = "Welcome to my personal website"
+++

Welcome to my personal website! This is where I share my thoughts, projects, and experiences.

## About Me

I'm a developer passionate about creating clean, efficient solutions.

<div id="career-timeline" style="width: 100%; height: 200px; margin: 10px 0;"></div>

<style>
/* Scoped to this chart only */
#career-timeline .highcharts-timeline-series .highcharts-point {
    stroke-width: 0;
}

#career-timeline .highcharts-timeline-series .highcharts-graph {
    stroke-width: 0;
}

#career-timeline .highcharts-timeline-series .highcharts-data-label {
    background: rgba(0, 0, 0, 0.8) !important;
    border: 1px solid rgba(255, 255, 255, 0.3) !important;
    border-radius: 6px !important;
    padding: 6px 10px !important;
    color: #ffffff !important;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif !important;
    font-weight: 600 !important;
    font-size: 12px !important;
    textOutline: 'none' !important;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4);
    backdrop-filter: blur(8px);
}

#career-timeline .highcharts-timeline-series .highcharts-data-label-box {
    background: transparent !important;
    border: none !important;
}

#career-timeline .highcharts-timeline-series .highcharts-data-label text {
    fill: #ffffff !important;
}
</style>

<script>
Highcharts.chart('career-timeline', {
    chart: {
        type: 'timeline',
        backgroundColor: 'transparent',
        height: 200, // Reduced from 300
        spacing: [2, 2, 2, 2], // Further reduced spacing
        margin: [5, 5, 5, 5], // Reduced margins
        style: {
            fontFamily: '-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif'
        }
    },
    title: null,
    subtitle: null,
    xAxis: {
        type: 'datetime',
        visible: false
    },
    yAxis: {
        visible: false
    },
    legend: {
        enabled: false
    },
    exporting: {
        enabled: false
    },
    plotOptions: {
        timeline: {
            dataLabels: {
                enabled: true,
                allowOverlap: false,
                format: '{point.company}',
                style: {
                    color: '#ffffff',
                    fontSize: '12px',
                    fontWeight: '600',
                    textOutline: 'none',
                    fontFamily: '-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif'
                },
                backgroundColor: 'rgba(0, 0, 0, 0.8)',
                borderColor: 'rgba(255, 255, 255, 0.3)',
                borderRadius: 6,
                borderWidth: 1,
                padding: 6
            },
            marker: {
                symbol: 'rect',
                radius: 8,
                lineWidth: 0,
                width: 20,
                height: 8
            },
            connectorWidth: 0,
            pointPadding: 0,
            groupPadding: 0,
            states: {
                hover: {
                    enabled: false
                }
            }
        }
    },
    tooltip: {
        enabled: true,
        useHTML: true,
        backgroundColor: 'rgba(0, 0, 0, 0.95)',
        borderColor: 'rgba(255, 255, 255, 0.3)',
        borderRadius: 8,
        borderWidth: 1,
        shadow: true,
        style: {
            color: '#ffffff',
            fontSize: '13px',
            fontFamily: '-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif'
        },
        formatter: function() {
            return '<div style="padding: 8px;">' +
                   '<div style="font-weight: 600; margin-bottom: 6px; color: #4A90E2;">' + this.point.name + '</div>' +
                   '<div style="margin-bottom: 4px;"><strong>Company:</strong> ' + this.point.company + '</div>' +
                   '<div style="margin-bottom: 4px;"><strong>Location:</strong> ' + this.point.location + '</div>' +
                   '<div style="margin-bottom: 4px;"><strong>Duration:</strong> ' + this.point.duration + '</div>' +
                   '<div style="margin-top: 8px; font-style: italic; color: #cccccc;">' + this.point.description + '</div>' +
                   '</div>';
        }
    },
    credits: {
        enabled: false
    },
    colors: ['#6BCF7F', '#FFD93D', '#FF6B6B', '#50C878', '#7B68EE', '#4A90E2'],
    series: [{
        name: 'Career Timeline',
        data: [{
            name: 'Data Science Bootcamp',
            company: 'Flatiron School',
            location: 'New York, NY',
            duration: 'Sep 2020 - Jan 2021',
            description: 'Immersive Data Science program',
            x: Date.UTC(2020, 8, 1)
        }, {
            name: 'Data Analyst (Fraud/Risk)',
            company: 'Snap Finance',
            location: 'Salt Lake City, UT',
            duration: 'Jun 2021 - Jan 2022',
            description: 'SQL analysis, R programming, automated executive reporting',
            x: Date.UTC(2021, 5, 1)
        }, {
            name: 'Data Scientist (Fraud)',
            company: 'Snap Finance',
            location: 'Salt Lake City, UT',
            duration: 'Jan 2022 - Jan 2023',
            description: 'Integrated DataVisor, developed XGBoost model, conducted fraud analysis',
            x: Date.UTC(2022, 0, 1)
        }, {
            name: 'Founding Analytics Engineer',
            company: 'Snap Finance',
            location: 'Salt Lake City, UT',
            duration: 'Feb 2023 - Apr 2024',
            description: 'Orchestrated data pipelines, developed CI/CD, implemented Looker dashboards',
            x: Date.UTC(2023, 1, 1)
        }, {
            name: 'Staff Analytics Engineer',
            company: 'Snap Finance (Seen)',
            location: 'Salt Lake City, UT',
            duration: 'Apr 2024 - Apr 2025',
            description: 'Designed change management framework, automated validation processes, enhanced CI/CD',
            x: Date.UTC(2024, 3, 1)
        }, {
            name: 'Senior Analytics Engineer',
            company: 'Weave',
            location: 'Lehi, UT',
            duration: 'Apr 2025 - Present',
            description: 'Led data model development, implemented Dagster orchestration, upskilled team members',
            x: Date.UTC(2025, 3, 1)
        }]
    }]
});
</script>

## Recent Posts

Check out my latest blog posts and journal entries below. 