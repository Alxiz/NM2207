library(shiny)

# Define UI for displaying current time ----
ui <- fluidPage(
  
  titlePanel(code("TIMER")),
  h2(textOutput("currentTime")),
  strong("The displayed time is Singapore-based"),
  img(src = "Flag_of_Singapore.svg.jpg", height = 600, width = 400)
)

# Define server logic to show current time, update every second ----
server <- function(input, output, session) {
  
  output$currentTime <- renderText({
    invalidateLater(1000, session)
    paste("The current time is", Sys.time())
  })
  
}


# Create Shiny app ----
shinyApp(ui, server)

