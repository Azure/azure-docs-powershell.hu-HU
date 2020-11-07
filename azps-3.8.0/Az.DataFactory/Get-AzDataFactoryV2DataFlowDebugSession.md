---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847305"
---
# <span data-ttu-id="3dcab-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3dcab-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="3dcab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3dcab-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcab-103">Az aktív adatfolyam-debug munkamenetek beszerzése az Azure Data Factory segítségével</span><span class="sxs-lookup"><span data-stu-id="3dcab-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="3dcab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3dcab-104">SYNTAX</span></span>

### <span data-ttu-id="3dcab-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3dcab-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dcab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3dcab-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3dcab-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3dcab-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dcab-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3dcab-108">DESCRIPTION</span></span>
<span data-ttu-id="3dcab-109">Az Azure Data Factory által az összes aktív adatfolyam debug-munkamenetének listázása adatokkal.</span><span class="sxs-lookup"><span data-stu-id="3dcab-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="3dcab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3dcab-110">EXAMPLES</span></span>

### <span data-ttu-id="3dcab-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3dcab-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="3dcab-112">Az Azure Data Factory "WikiADF" minden aktív adatfolyam-hibakeresési munkamenetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="3dcab-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="3dcab-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3dcab-113">PARAMETERS</span></span>

### <span data-ttu-id="3dcab-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3dcab-114">-DataFactory</span></span>
<span data-ttu-id="3dcab-115">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="3dcab-115">The data factory object.</span></span>

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

### <span data-ttu-id="3dcab-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3dcab-116">-DataFactoryName</span></span>
<span data-ttu-id="3dcab-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="3dcab-117">The data factory name.</span></span>

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

### <span data-ttu-id="3dcab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcab-118">-DefaultProfile</span></span>
<span data-ttu-id="3dcab-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3dcab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dcab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dcab-120">-ResourceGroupName</span></span>
<span data-ttu-id="3dcab-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3dcab-121">The resource group name.</span></span>

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

### <span data-ttu-id="3dcab-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dcab-122">-ResourceId</span></span>
<span data-ttu-id="3dcab-123">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="3dcab-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3dcab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcab-124">CommonParameters</span></span>
<span data-ttu-id="3dcab-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3dcab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcab-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3dcab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcab-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dcab-127">INPUTS</span></span>

### <span data-ttu-id="3dcab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3dcab-128">System.String</span></span>

### <span data-ttu-id="3dcab-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3dcab-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3dcab-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dcab-130">OUTPUTS</span></span>

### <span data-ttu-id="3dcab-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="3dcab-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="3dcab-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3dcab-132">NOTES</span></span>
<span data-ttu-id="3dcab-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="3dcab-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3dcab-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dcab-134">RELATED LINKS</span></span>

[<span data-ttu-id="3dcab-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3dcab-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="3dcab-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="3dcab-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="3dcab-137">Meghívó-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="3dcab-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="3dcab-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3dcab-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)