ETracker
router.get('/api', authorized, function(req, res) {
router.get('/api/employee/', authorized, function(req, res) {
router.get('/api/employee/:id', authorized, function(req, res) {
router.get('/api/employee/:id/training', authorized, function(req, res) {
router.get('/api/department', authorized, function(req, res) {
router.get('/api/department/:name', authorized, function(req, res) {
router.get('/api/department/:name/training', authorized, function(req, res) {
router.get('/api/training', authorized, function(req, res) {
router.get('/api/training/:name/department', authorized, function(req, res) {
router.get('/api/training/:name/employee', authorized, function(req, res) {

// Save training
router.post('/api/training', authorized, function(req, res) {
// Assign training to department and its employees
router.post('/api/training/department', authorized, function(req, res) {
// Assign training to individual employee
router.post('/api/training/employee', authorized, function(req, res) {

Using MySQLWorkbench

	DROP DATABASE etracker_db;
	CREATE DATABASE etracker_db;
	USE etracker_db;


Edit server.js line 20 change false to true
	Using Console
		start server ->	node server.js
		kill server  -> Ctrl C

Edit server.js line 20 change true to false
	Using Console
		sequelize db:migrate
		sequelize db:seed:all
		start server ->	node server.js	
		goto -> localhost:7070