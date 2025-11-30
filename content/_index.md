+++
title = "Brendan Ferris"
description = "Welcome to my personal website"
+++

Welcome to my site. I post here as an outlet for work that is outside of my normal day-to-day engineering tasks. Some older projects can also be found <a href="https://medium.com/@brendanfrrs" target="_blank">here</a>.

## About Me

My technical career began about {{ years_since(start_year=2021) }} years ago. I was working as a private investigator in the New York/New Jersey area focusing mainly on insurance fraud. I became interested in understanding the ways insurance companies mitigated fraudulent waste through analytics and data science. This led me to take up a role on the fraud team at a fintech company in Salt Lake City, Utah -- where I am still based. I most liked the cat-and-mouse aspect of working in the fraud space, and being an analyst gave me a good technical base when I was promoted to the data science team. As a data scientist I was able to utilize predictive analytics to combat payment chargebacks, and exploratory analysis to understand fraud trends and causes.

I began to notice that I really spent most of my time as a data scientist trying to get the data in the proper format for predictive analytics. As is normal in most mid-size companies, data was dispersed and managed by teams often working within silos.

When my company had acquired a credit card startup in Berlin I was appointed to be one of the founding engineers. The task was straight forward, "wind down" the existing customer base and re-launch under a new name and with improved business processes. It was here that my focus shifted toward data engineering, data infrastructure, and data platforms. I became very interested in improving the experience of data scientists, data analysts, and business users. This is also currently where I devote the majority of my time. 

<div style="width: 100%; overflow-x: auto; overflow-y: hidden; margin: 20px 0 10px 0;">
    <div id="career-timeline" style="min-width: 1400px; height: 180px; overflow: visible;"></div>
</div>

<style>
#career-timeline {
    min-height: 180px;
    overflow: visible !important;
}

#career-timeline .highcharts-container {
    overflow: visible !important;
}

#career-timeline .highcharts-xaxis-labels text {
    fill: currentColor !important;
    opacity: 0.85 !important;
    font-weight: 600 !important;
    font-size: 11px !important;
}

#career-timeline .highcharts-series rect {
    stroke: rgba(255, 255, 255, 0.3);
    stroke-width: 1;
    filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.3));
}

/* Ensure tooltip doesn't get clipped */
.highcharts-tooltip {
    z-index: 9999 !important;
}

/* Style the scrollbar for better appearance */
#career-timeline::-webkit-scrollbar {
    height: 8px;
}

#career-timeline::-webkit-scrollbar-track {
    background: rgba(255, 255, 255, 0.1);
    border-radius: 4px;
}

#career-timeline::-webkit-scrollbar-thumb {
    background: rgba(255, 255, 255, 0.3);
    border-radius: 4px;
}

#career-timeline::-webkit-scrollbar-thumb:hover {
    background: rgba(255, 255, 255, 0.5);
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
    if (typeof Highcharts === 'undefined') {
        console.error('Highcharts not loaded');
        return;
    }
    
    Highcharts.chart('career-timeline', {
        chart: {
            type: 'xrange',
            backgroundColor: 'transparent',
            height: 180,
            spacing: [15, 15, 15, 15],
            margin: [15, 15, 35, 15]
        },
        title: null,
        xAxis: {
            type: 'datetime',
            labels: {
                style: { 
                    color: '#1f2937',
                    fontSize: '11px',
                    fontWeight: '600'
                },
                y: 20
            },
            lineWidth: 1,
            lineColor: 'var(--border, rgba(128, 128, 128, 0.3))',
            tickLength: 5,
            tickColor: 'var(--border, rgba(128, 128, 128, 0.3))',
            gridLineWidth: 0
        },
        yAxis: {
            title: null,
            categories: ['Career'],
            visible: false
        },
        legend: { enabled: false },
        credits: { enabled: false },
        exporting: { enabled: false },
        plotOptions: {
            xrange: {
                borderRadius: 8,
                pointPadding: 0,
                groupPadding: 0,
                dataLabels: {
                    enabled: true,
                    inside: true,
                    useHTML: true,
                    align: 'left',
                    verticalAlign: 'middle',
                    padding: 0,
                    overflow: 'allow',
                    crop: false,
                    style: { 
                        textOutline: 'none',
                        width: '100%'
                    },
                    formatter: function() {
                        const width = this.point.shapeArgs.width;
                        const titleLength = this.point.name.length;
                        const companyLength = this.point.company.length;
                        
                        // Dynamic font sizing: calculate based on available width per character
                        // Aim for roughly 5-7 pixels per character for readability
                        let titleSize = Math.max(5.5, Math.min(11, (width - 20) / (titleLength * 0.6)));
                        let companySize = Math.max(5, Math.min(9, (width - 20) / (companyLength * 0.65)));
                        
                        // For very narrow bars, scale down more aggressively
                        if (width < 120) {
                            titleSize = Math.max(5, Math.min(8, (width - 16) / (titleLength * 0.55)));
                            companySize = Math.max(4.5, Math.min(7, (width - 16) / (companyLength * 0.6)));
                        }
                        
                        // Left-align text with proper wrapping and vertical centering
                        return '<div style="width: ' + (width - 14) + 'px; padding: 5px 7px; color: #fff; text-align: left; line-height: 1.15; text-shadow: 0 1px 3px rgba(0,0,0,0.7); display: flex; flex-direction: column; justify-content: center; height: 100%;">' +
                               '<div style="font-size: ' + titleSize + 'px; font-weight: 700; margin-bottom: 1px; word-wrap: break-word; overflow-wrap: break-word;">' + this.point.name + '</div>' +
                               '<div style="font-size: ' + companySize + 'px; font-weight: 500; opacity: 0.95; word-wrap: break-word; overflow-wrap: break-word; line-height: 1.1;">' + this.point.company + '</div>' +
                               '</div>';
                    }
                },
                states: {
                    hover: { 
                        brightness: 0.15,
                        borderColor: 'rgba(255, 255, 255, 0.5)',
                        borderWidth: 2
                    }
                }
            }
        },
        tooltip: {
            useHTML: true,
            backgroundColor: 'rgba(0, 0, 0, 0.95)',
            borderColor: 'rgba(255, 255, 255, 0.3)',
            borderRadius: 10,
            borderWidth: 1,
            padding: 0,
            outside: true,
            hideDelay: 500,
            stickOnContact: true,
            shadow: {
                color: 'rgba(0, 0, 0, 0.5)',
                offsetX: 0,
                offsetY: 4,
                width: 10
            },
            style: { 
                color: '#ffffff',
                fontSize: '13px',
                fontFamily: '-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif',
                pointerEvents: 'auto'
            },
            formatter: function() {
                const companyLink = this.point.website ? 
                    '<a href="' + this.point.website + '" target="_blank" rel="noopener noreferrer" style="color: ' + this.point.color + '; text-decoration: none; border-bottom: 2px solid ' + this.point.color + '; transition: opacity 0.2s;" onmouseover="this.style.opacity=\'0.7\'" onmouseout="this.style.opacity=\'1\'">' + this.point.company + '</a>' :
                    '<span style="color: ' + this.point.color + ';">' + this.point.company + '</span>';
                
                return '<div style="width: 240px; padding: 14px 16px; box-sizing: border-box; line-height: 1.5;">' +
                       '<div style="font-weight: 700; font-size: 15px; margin-bottom: 10px; line-height: 1.3; word-wrap: break-word; overflow-wrap: break-word;">' + 
                       this.point.name + 
                       '</div>' +
                       '<div style="font-size: 12px; margin-bottom: 8px; word-wrap: break-word; overflow-wrap: break-word;">' +
                       '<span style="color: rgba(255, 255, 255, 0.7);">at</span> <strong>' + companyLink + '</strong>' +
                       '</div>' +
                       '<div style="font-size: 11px; color: rgba(255, 255, 255, 0.85); margin-bottom: 3px; word-wrap: break-word; overflow-wrap: break-word;">' +
                       '📍 ' + this.point.location +
                       '</div>' +
                       '<div style="font-size: 11px; color: rgba(255, 255, 255, 0.85); margin-bottom: 10px;">' +
                       '📅 ' + this.point.duration +
                       '</div>' +
                       '<div style="font-size: 11px; color: rgba(255, 255, 255, 0.9); line-height: 1.5; padding-top: 10px; border-top: 1px solid rgba(255, 255, 255, 0.2); word-wrap: break-word; overflow-wrap: break-word; white-space: normal;">' +
                       this.point.description +
                       '</div>' +
                       '</div>';
            }
        },
        series: [{
            name: 'Career',
            pointWidth: 70,
            data: [
                {
                    x: Date.UTC(2020, 8, 1),
                    x2: Date.UTC(2021, 0, 31),
                    y: 0,
                    name: 'Data Science Bootcamp',
                    company: 'Flatiron School',
                    website: 'https://flatironschool.com',
                    location: 'New York',
                    duration: 'Sep 2020 - Jan 2021',
                    description: 'Completed an immersive Data Science program covering Python, SQL, machine learning, and statistical analysis.',
                    color: '#059669'
                },
                {
                    x: Date.UTC(2021, 5, 1),
                    x2: Date.UTC(2022, 0, 31),
                    y: 0,
                    name: 'Data Analyst',
                    company: 'Snap Finance',
                    website: 'https://www.snapfinance.com',
                    location: 'Salt Lake City',
                    duration: 'Jun 2021 - Jan 2022',
                    description: 'Performed SQL analysis and R programming to automate executive reporting and detect fraud patterns. Supported the operations and executive fraud teams.',
                    color: '#D97706'
                },
                {
                    x: Date.UTC(2022, 0, 1),
                    x2: Date.UTC(2023, 0, 31),
                    y: 0,
                    name: 'Data Scientist',
                    company: 'Snap Finance',
                    website: 'https://www.snapfinance.com',
                    location: 'Salt Lake City',
                    duration: 'Jan 2022 - Jan 2023',
                    description: 'Integrated DataVisor for fraud detection and developed XGBoost models to improve payment chargeback review process.',
                    color: '#DC2626' 
                },
                {
                    x: Date.UTC(2023, 1, 1),
                    x2: Date.UTC(2024, 3, 30),
                    y: 0,
                    name: 'Founding Analytics Engineer',
                    company: 'Seen Finance',
                    website: 'https://www.seen.com',
                    location: 'Salt Lake City | Berlin',
                    duration: 'Feb 2023 - Apr 2024',
                    description: 'Built the analytics foundation from scratch, orchestrating data pipelines with Prefect, warehouse manipulations with dbt and BigQuery developing CI/CD workflows, and implementing Looker dashboards.',
                    color: '#0D9488'
                },
                {
                    x: Date.UTC(2024, 3, 1),
                    x2: Date.UTC(2025, 3, 30),
                    y: 0,
                    name: 'Staff Analytics Engineer',
                    company: 'Seen Finance',
                    website: 'https://www.seen.com',
                    location: 'Salt Lake City | Berlin',
                    duration: 'Apr 2024 - Apr 2025',
                    description: 'Led the design of a change management framework, automated validation processes, and enhanced CI/CD pipelines for production reliability, grew foundational analytics team by one member.',
                    color: '#7C3AED'
                },
                {
                    x: Date.UTC(2025, 3, 1),
                    x2: new Date().getTime(),
                    y: 0,
                    name: 'Senior Analytics Engineer',
                    company: 'Weave',
                    website: 'https://www.getweave.com',
                    location: 'Lehi, UT',
                    duration: 'Apr 2025 - Present',
                    description: 'Leading data model development, re-writing ELT pipelines in Dagster, mentoring team members on best practices, transitioning team from reactive to proactive.',
                    color: '#2563EB'  // Deeper blue - strong contrast
                }
            ]
        }]
    });
});
</script>

<!-- Skills -->
# Skills

<div id="skills-chart" style="width: 100%; max-width: 600px; height: 500px; margin: 40px auto;"></div>

<style>
#skills-chart .highcharts-grid-line {
    stroke: currentColor !important;
    opacity: 0.2 !important;
}

#skills-chart .highcharts-axis-labels text {
    fill: currentColor !important;
}
</style>


<script>
document.addEventListener('DOMContentLoaded', function() {
    if (typeof Highcharts === 'undefined') return;
    
    Highcharts.chart('skills-chart', {
        chart: {
            polar: true,
            type: 'line',
            backgroundColor: 'transparent'
        },
        
        title: {
            text: null
        },
        
        pane: {
            size: '80%'
        },
        
        xAxis: {
            categories: [
                'Python', 
                'SQL', 
                'dbt', 
                'GCP', 
                'Prefect', 
                'Dagster', 
                'Looker', 
                'Sigma', 
                'GitHub Actions',
            ],
            tickmarkPlacement: 'on',
            lineWidth: 0,
            gridLineColor: 'currentColor',
            gridLineWidth: 1,
            labels: {
                style: {
                    color: 'currentColor',
                    fontSize: '12px',
                    fontWeight: '500'
                }
            }
        },
        
        yAxis: {
            gridLineInterpolation: 'polygon',
            lineWidth: 0,
            min: 0,
            max: 10,
            tickInterval: 2,
            gridLineColor: 'currentColor',
            gridLineWidth: 1,
            labels: {
                style: {
                    color: 'currentColor',
                    fontSize: '10px'
                }
            }
        },
        
        tooltip: {
            backgroundColor: 'rgba(0, 0, 0, 0.9)',
            borderColor: 'rgba(255, 255, 255, 0.3)',
            borderRadius: 8,
            padding: 12,
            style: { 
                color: '#fff',
                fontSize: '13px'
            },
            useHTML: true,
            formatter: function() {
                return '<div style="width: 220px; word-wrap: break-word; overflow-wrap: break-word;">' +
                    '<strong style="font-size: 14px; color: ' + this.point.color + ';">' + 
                    this.point.name + '</strong><br/>' +
                    '<span style="font-size: 16px; font-weight: 600; margin: 8px 0; display: block;">' + 
                    this.point.y + '/10</span>' +
                    '<p style="margin: 8px 0 0 0; line-height: 1.5; color: rgba(255,255,255,0.9); white-space: normal;">' + 
                    this.point.description + '</p>' +
                    '</div>';
            }
        },
        
        legend: {
            enabled: false
        },
        
        series: [{
            name: 'Proficiency',
            data: [
                {
                    y: 6.5,
                    name: 'Python',
                    description: 'Advanced proficiency in data engineering, automation, and building ETL pipelines'
                },
                {
                    y: 7,
                    name: 'SQL',
                    description: 'Expert in complex queries, optimization, and database design for analytics'
                },
                {
                    y: 9.5,
                    name: 'dbt',
                    description: 'Extensive experience building and maintaining data transformation pipelines'
                },
                {
                    y: 5,
                    name: 'GCP',
                    description: 'Proficient with BigQuery, Cloud Storage, and data services'
                },
                {
                    y: 7,
                    name: 'Prefect',
                    description: 'Experience orchestrating data workflows and managing dependencies'
                },
                {
                    y: 5,
                    name: 'Dagster',
                    description: 'Building and deploying data pipelines with asset-based orchestration'
                },
                {
                    y: 7,
                    name: 'Looker',
                    description: 'Creating dashboards, LookML modeling, and business intelligence'
                },
                {
                    y: 3,
                    name: 'Sigma',
                    description: 'Building interactive analytics dashboards for business users'
                },
                {
                    y: 6,
                    name: 'GitHub Actions',
                    description: 'CI/CD pipeline automation and workflow orchestration'
                }
            ],
            pointPlacement: 'on',
            color: '#8B5CF6',
            fillOpacity: 0.15,
            lineWidth: 2,
            marker: {
                radius: 4,
                fillColor: 'rgba(139, 92, 246, 0.5)',
                lineColor: '#8B5CF6',
                lineWidth: 2
            }
        }],
        
        exporting: {
            enabled: false
        },
        
        credits: {
            enabled: false
        }
    });
});
</script>

## Recent Posts