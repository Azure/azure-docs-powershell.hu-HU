---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505415"
---
# <span data-ttu-id="45291-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="45291-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="45291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45291-102">SYNOPSIS</span></span>
<span data-ttu-id="45291-103">Egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="45291-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45291-104">SYNTAX</span></span>

### <span data-ttu-id="45291-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45291-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45291-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="45291-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45291-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="45291-107">DESCRIPTION</span></span>
<span data-ttu-id="45291-108">A **New-AzureRmOperationalInsightsCustomLogDataSource** parancsmag egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="45291-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="45291-109">Példák</span><span class="sxs-lookup"><span data-stu-id="45291-109">EXAMPLES</span></span>

## <span data-ttu-id="45291-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45291-110">PARAMETERS</span></span>

### <span data-ttu-id="45291-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="45291-111">-CustomLogRawJson</span></span>
<span data-ttu-id="45291-112">Az egyéni webhelycsoport-házirendet adja meg nyers JavaScript-objektumként (JSON) karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="45291-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45291-113">-DefaultProfile</span></span>
<span data-ttu-id="45291-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45291-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45291-115">-Force</span><span class="sxs-lookup"><span data-stu-id="45291-115">-Force</span></span>
<span data-ttu-id="45291-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="45291-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45291-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45291-117">-Name</span></span>
<span data-ttu-id="45291-118">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45291-118">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45291-119">-ResourceGroupName</span></span>
<span data-ttu-id="45291-120">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45291-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-121">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="45291-121">-Workspace</span></span>
<span data-ttu-id="45291-122">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="45291-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="45291-123">-WorkspaceName</span></span>
<span data-ttu-id="45291-124">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="45291-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45291-125">-Confirm</span></span>
<span data-ttu-id="45291-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45291-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45291-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45291-127">-WhatIf</span></span>
<span data-ttu-id="45291-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45291-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45291-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45291-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45291-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45291-130">CommonParameters</span></span>
<span data-ttu-id="45291-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45291-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45291-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45291-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45291-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45291-133">INPUTS</span></span>

### <span data-ttu-id="45291-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="45291-134">PSWorkspace</span></span>
<span data-ttu-id="45291-135">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="45291-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="45291-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45291-136">OUTPUTS</span></span>

### <span data-ttu-id="45291-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="45291-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="45291-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45291-138">NOTES</span></span>

## <span data-ttu-id="45291-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45291-139">RELATED LINKS</span></span>

[<span data-ttu-id="45291-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="45291-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="45291-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="45291-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


