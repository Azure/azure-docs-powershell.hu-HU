---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477170"
---
# <span data-ttu-id="a54c9-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a54c9-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="a54c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a54c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a54c9-103">Az összes aktív adatfolyam-hibakeresési munkamenet lekérte az Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="a54c9-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="a54c9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a54c9-104">SYNTAX</span></span>

### <span data-ttu-id="a54c9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a54c9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a54c9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a54c9-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a54c9-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a54c9-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a54c9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a54c9-108">DESCRIPTION</span></span>
<span data-ttu-id="a54c9-109">Az összes aktív adatfolyam-hibakeresési munkamenet felsorolása az Azure Data Factory szerint részletes információkkal.</span><span class="sxs-lookup"><span data-stu-id="a54c9-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="a54c9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a54c9-110">EXAMPLES</span></span>

### <span data-ttu-id="a54c9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a54c9-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="a54c9-112">Az összes aktív adatfolyam-hibakeresési munkamenet lekérte az Azure Data Factory "WikiADF" szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="a54c9-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="a54c9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a54c9-113">PARAMETERS</span></span>

### <span data-ttu-id="a54c9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a54c9-114">-DataFactory</span></span>
<span data-ttu-id="a54c9-115">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="a54c9-115">The data factory object.</span></span>

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

### <span data-ttu-id="a54c9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a54c9-116">-DataFactoryName</span></span>
<span data-ttu-id="a54c9-117">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="a54c9-117">The data factory name.</span></span>

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

### <span data-ttu-id="a54c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54c9-118">-DefaultProfile</span></span>
<span data-ttu-id="a54c9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a54c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a54c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="a54c9-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a54c9-121">The resource group name.</span></span>

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

### <span data-ttu-id="a54c9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a54c9-122">-ResourceId</span></span>
<span data-ttu-id="a54c9-123">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="a54c9-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a54c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54c9-124">CommonParameters</span></span>
<span data-ttu-id="a54c9-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a54c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54c9-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a54c9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54c9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a54c9-127">INPUTS</span></span>

### <span data-ttu-id="a54c9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a54c9-128">System.String</span></span>

### <span data-ttu-id="a54c9-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a54c9-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a54c9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a54c9-130">OUTPUTS</span></span>

### <span data-ttu-id="a54c9-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="a54c9-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="a54c9-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a54c9-132">NOTES</span></span>
<span data-ttu-id="a54c9-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="a54c9-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a54c9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a54c9-134">RELATED LINKS</span></span>

[<span data-ttu-id="a54c9-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a54c9-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a54c9-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a54c9-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="a54c9-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="a54c9-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="a54c9-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a54c9-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)