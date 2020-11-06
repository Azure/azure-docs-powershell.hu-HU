---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e9d5a7443c8a758cdc839826025d51fe57d55420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498212"
---
# <span data-ttu-id="c2c63-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c2c63-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="c2c63-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2c63-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c63-103">Törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="c2c63-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2c63-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2c63-104">SYNTAX</span></span>

### <span data-ttu-id="c2c63-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2c63-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c63-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2c63-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c63-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2c63-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c63-108">A **Remove-AzureRmOperationalInsightsDataSource** parancsmag törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="c2c63-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="c2c63-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2c63-109">EXAMPLES</span></span>

## <span data-ttu-id="c2c63-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2c63-110">PARAMETERS</span></span>

### <span data-ttu-id="c2c63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c63-111">-DefaultProfile</span></span>
<span data-ttu-id="c2c63-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c2c63-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c2c63-113">-Force</span></span>
<span data-ttu-id="c2c63-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c2c63-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2c63-115">-Name</span></span>
<span data-ttu-id="c2c63-116">A törlendő adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2c63-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c63-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2c63-118">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2c63-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-119">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="c2c63-119">-Workspace</span></span>
<span data-ttu-id="c2c63-120">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="c2c63-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2c63-121">-WorkspaceName</span></span>
<span data-ttu-id="c2c63-122">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="c2c63-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2c63-123">-Confirm</span></span>
<span data-ttu-id="c2c63-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2c63-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c63-125">-WhatIf</span></span>
<span data-ttu-id="c2c63-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c2c63-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c63-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2c63-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c63-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c63-128">CommonParameters</span></span>
<span data-ttu-id="c2c63-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2c63-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c63-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c63-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c63-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2c63-131">INPUTS</span></span>

### <span data-ttu-id="c2c63-132">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2c63-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="c2c63-133">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2c63-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="c2c63-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c2c63-134">System.String</span></span>

## <span data-ttu-id="c2c63-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2c63-135">OUTPUTS</span></span>

### <span data-ttu-id="c2c63-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="c2c63-136">System.Void</span></span>

## <span data-ttu-id="c2c63-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2c63-137">NOTES</span></span>
* <span data-ttu-id="c2c63-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="c2c63-138">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c2c63-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2c63-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2c63-140">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c2c63-140">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="c2c63-141">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c2c63-141">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


