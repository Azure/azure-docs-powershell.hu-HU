---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 1521f0f4f3b90010e24185a036dca047860e27c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667063"
---
# <span data-ttu-id="f323a-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f323a-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="f323a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f323a-102">SYNOPSIS</span></span>
<span data-ttu-id="f323a-103">Az aktív adatfolyam-debug munkamenetek beszerzése az Azure Data Factory segítségével</span><span class="sxs-lookup"><span data-stu-id="f323a-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="f323a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f323a-104">SYNTAX</span></span>

### <span data-ttu-id="f323a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f323a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f323a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f323a-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f323a-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f323a-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f323a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f323a-108">DESCRIPTION</span></span>
<span data-ttu-id="f323a-109">Az Azure Data Factory által az összes aktív adatfolyam debug-munkamenetének listázása adatokkal.</span><span class="sxs-lookup"><span data-stu-id="f323a-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="f323a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f323a-110">EXAMPLES</span></span>

### <span data-ttu-id="f323a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f323a-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="f323a-112">Az Azure Data Factory "WikiADF" minden aktív adatfolyam-hibakeresési munkamenetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="f323a-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="f323a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f323a-113">PARAMETERS</span></span>

### <span data-ttu-id="f323a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f323a-114">-DataFactory</span></span>
<span data-ttu-id="f323a-115">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="f323a-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f323a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f323a-116">-DataFactoryName</span></span>
<span data-ttu-id="f323a-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="f323a-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f323a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f323a-118">-DefaultProfile</span></span>
<span data-ttu-id="f323a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f323a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f323a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f323a-120">-ResourceGroupName</span></span>
<span data-ttu-id="f323a-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f323a-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f323a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f323a-122">-ResourceId</span></span>
<span data-ttu-id="f323a-123">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f323a-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f323a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f323a-124">CommonParameters</span></span>
<span data-ttu-id="f323a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f323a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f323a-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f323a-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f323a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f323a-127">INPUTS</span></span>

### <span data-ttu-id="f323a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f323a-128">System.String</span></span>

### <span data-ttu-id="f323a-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f323a-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f323a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f323a-130">OUTPUTS</span></span>

### <span data-ttu-id="f323a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="f323a-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="f323a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f323a-132">NOTES</span></span>
<span data-ttu-id="f323a-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="f323a-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f323a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f323a-134">RELATED LINKS</span></span>

[<span data-ttu-id="f323a-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f323a-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="f323a-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="f323a-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="f323a-137">Meghívó-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="f323a-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="f323a-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f323a-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)