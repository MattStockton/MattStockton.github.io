---
title: "Writing"
layout: collection
collection: posts
entries_layout: list
classes: 
  - wide
---

<style>
  /* Force full width container without indentation */
  .page__content,
  .archive,
  #main {
    max-width: 1200px !important;
    margin-left: auto !important;
    margin-right: auto !important;
    float: none !important;
    width: 100% !important;
  }

  /* Remove any right-side shifting */
  #main {
    padding-left: 1em !important;
    padding-right: 1em !important;
  }
  
  /* Container for better spacing */
  .archive {
    margin-top: 1.5em;
  }
  
  /* Post card styling */
  .archive__item {
    padding: 1em 1.4em;
    margin-bottom: 1.4em;
    background-color: #fff;
    border-radius: 6px;
    box-shadow: rgba(0, 0, 0, 0.04) 0px 3px 8px;
    border-top: 3px solid #0A4D68; /* PragmaNexus primary color */
    transition: transform 0.2s ease-out;
  }
  
  /* Subtle lift effect on hover */
  .archive__item:hover {
    transform: translateY(-2px);
    box-shadow: rgba(0, 0, 0, 0.08) 0px 4px 12px;
  }
  
  /* Post title styling */
  .archive__item-title {
    margin-top: 0.1em !important;
    margin-bottom: 0.4em !important;
    font-size: 1.35em !important;
    letter-spacing: -0.01em !important;
  }
  
  /* Title link styling */
  .archive__item-title a {
    color: #0A4D68 !important; /* PragmaNexus primary color */
    text-decoration: none !important;
    transition: color 0.2s ease;
  }
  
  .archive__item-title a:hover {
    color: #137a9e !important; /* Lighter shade of primary for hover */
  }
  
  /* Meta information styling */
  .page__meta {
    margin-bottom: 0.5em !important;
    font-size: 0.85em !important;
    color: #6c757d !important;
    font-weight: 400 !important;
  }
  
  /* Ensure excerpts are displayed by overriding any theme settings that might hide them */
  .archive__item-excerpt {
    display: block !important;
    margin-top: 0.6em !important;
    margin-bottom: 0.6em !important;
    font-size: 0.92em !important;
    color: #212529 !important; /* PragmaNexus text color */
    line-height: 1.55 !important;
  }
  
  /* Button styling */
  .btn--primary {
    padding: 0.35em 0.9em !important;
    font-size: 0.78em !important;
    background-color: #fff !important;
    color: #0A4D68 !important; /* PragmaNexus primary color */
    border: 1px solid #0A4D68 !important; /* PragmaNexus primary color */
    border-radius: 4px !important;
    transition: all 0.2s ease !important;
  }
  
  /* Button hover effect */
  .btn--primary:hover {
    background-color: #0A4D68 !important; /* PragmaNexus primary color */
    color: #fff !important;
  }
  
  /* Ensure page title is styled nicely */
  .page__title {
    margin-bottom: 0.8em !important;
    color: #0A4D68 !important; /* PragmaNexus primary color */
  }

  /* Fix position of sidebar if present */
  .sidebar__right {
    display: none !important;
  }
</style>