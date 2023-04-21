
BIN     = omnetpp2017

CXX      = CC -fast
CXXFLAGS = 
EXTRA_CXXFLAGS = -I src -I src/model -I src/simulator -I src/simulator/platdep \
                 -DSPEC -DNDEBUG -DWITH_NETBUILDER -DSPEC_AUTO_SUPPRESS_OPENMP
LIBS = -static

# rate  -DSPEC_AUTO_SUPPRESS_OPENMP
# speed -DSPEC_OPENMP

SOURCES =  \
    fileoutscalarmgr.cc \
    xmlgenerator.cc \
    cdisplaystring.cc \
    expression.tab.cc \
    patternmatcher.cc \
    neddtdvalidator.cc \
    cmessage.cc \
    cenvir.cc \
    matchableobject.cc \
    cstringpool.cc \
    nedyylib.cc \
    cgate.cc \
    cconfiguration.cc \
    cdynamicchanneltype.cc \
    cxmlparimpl.cc \
    nedexception.cc \
    csimulation.cc \
    msg2.tab.cc \
    spec_qsort.cc \
    nedelements.cc \
    cdataratechannel.cc \
    clcg32.cc \
    envirbase.cc \
    scenario.cc \
    cstringtokenizer.cc \
    appreg.cc \
    nedsupport.cc \
    cvisitor.cc \
    valueiterator.cc \
    cmodule.cc \
    matchablefield.cc \
    nederror.cc \
    chasher.cc \
    cwatch.cc \
    cparimpl.cc \
    globals.cc \
    cstringparimpl.cc \
    speedometer.cc \
    fnamelisttokenizer.cc \
    nedvalidator.cc \
    cpacketqueue.cc \
    ned1generator.cc \
    nedparser.cc \
    ned1.tab.cc \
    ccompoundmodule.cc \
    eventlogwriter.cc \
    cexpressionbuilder.cc \
    cconfigoption.cc \
    cvarhist.cc \
    objectprinter.cc \
    main.cc \
    lex.expryy.cc \
    startup.cc \
    nedutil.cc \
    cmathfunction.cc \
    eventlogfilemgr.cc \
    nedtypeinfo.cc \
    cdoubleparimpl.cc \
    chistogram.cc \
    akaroarng.cc \
    cmessageheap.cc \
    simtime.cc \
    lex.msg2yy.cc \
    cregistrationlist.cc \
    cdetect.cc \
    csimplemodule.cc \
    expression.cc \
    lcgrandom.cc \
    inifilereader.cc \
    errmsg.cc \
    carray.cc \
    runattributes.cc \
    expr.tab.cc \
    sectionbasedconfig.cc \
    ccommbuffer.cc \
    clongparimpl.cc \
    cmsgpar.cc \
    cnamedobject.cc \
    cksplit.cc \
    cxmlelement.cc \
    ned2generator.cc \
    cboolparimpl.cc \
    cdelaychannel.cc \
    cenum.cc \
    onstartup.cc \
    cfsm.cc \
    lex.expressionyy.cc \
    fsutils.cc \
    nedfilebuffer.cc \
    cdynamicmoduletype.cc \
    displaystring.cc \
    enumstr.cc \
    cdensityestbase.cc \
    ctopology.cc \
    cnednetworkbuilder.cc \
    fileglobber.cc \
    cproperties.cc \
    cexception.cc \
    cxmldoccache.cc \
    saxparser_none.cc \
    cparsimcomm.cc \
    stringutil.cc \
    cownedobject.cc \
    linetokenizer.cc \
    nedelement.cc \
    cneddeclaration.cc \
    cdynamicexpression.cc \
    cnedfunction.cc \
    cproperty.cc \
    lex.ned1yy.cc \
    bigdecimal.cc \
    ccomponent.cc \
    clinkedlist.cc \
    nedtools.cc \
    opp_run.cc \
    nedsaxhandler.cc \
    matchexpression.tab.cc \
    cnedloader.cc \
    cpar.cc \
    nedresourcecache.cc \
    nedxmlparser.cc \
    task.cc \
    cclassdescriptor.cc \
    minixpath.cc \
    cstlwatch.cc \
    coutvector.cc \
    args.cc \
    cqueue.cc \
    ned2.tab.cc \
    nedsyntaxvalidator.cc \
    matchexpression.cc \
    cclassfactory.cc \
    exception.cc \
    fileutil.cc \
    distrib.cc \
    cstddev.cc \
    stringtokenizer.cc \
    matchexpressionlexer.cc \
    cstatistic.cc \
    neddtdvalidatorbase.cc \
    nedcrossvalidator.cc \
    ccomponenttype.cc \
    cobject.cc \
    cchannel.cc \
    akoutvectormgr.cc \
    filesnapshotmgr.cc \
    lex.ned2yy.cc \
    ccoroutine.cc \
    unitconversion.cc \
    cdefaultlist.cc \
    util.cc \
    commonutil.cc \
    cscheduler.cc \
    nedfunctions.cc \
    cmersennetwister.cc \
    sim_std_m.cc \
    filereader.cc \
    stringpool.cc \
    cmdenv.cc \
    fileoutvectormgr.cc \
    cpsquare.cc \
    indexedfileoutvectormgr.cc \
    intervals.cc \
    MACRelayUnitBase.cc \
    Ieee802Ctrl_m.cc \
    EtherEncap.cc \
    MACAddress.cc \
    EtherLLC.cc \
    EtherFrame_m.cc \
    EtherMAC.cc \
    MACRelayUnitNP.cc \
    EtherApp_m.cc \
    EtherMACBase.cc \
    EtherAppSrv.cc \
    MACRelayUnitPP.cc \
    EtherHub.cc \
    EtherAppCli.cc

OBJ     = $(SOURCES:.cc=.o)

VPATH = src/simulator:src/model

$(BIN): x$(BIN) $(BIN).execute.script
	cp $(BIN).execute.script $(BIN)
x$(BIN): $(OBJ)
	$(CXX) $(CXXFLAGS) -o x$(BIN) $(OBJ) $(LDFLAGS) $(LIBS)

.cc.o:
	$(CXX) -c $(EXTRA_CXXFLAGS) $(CXXFLAGS) $<

clean:
	-rm -f core
	-rm -f $(OBJ)

clobber: clean
	-rm -f $(BIN) x$(BIN) General-0.sca omnetpp.ini
