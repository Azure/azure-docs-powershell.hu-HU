---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 49674f372e477ee7050a6ccf7d833aaee59bac3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494754"
---
# <span data-ttu-id="53040-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="53040-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="53040-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53040-102">SYNOPSIS</span></span>
<span data-ttu-id="53040-103">Törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="53040-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53040-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53040-104">SYNTAX</span></span>

### <span data-ttu-id="53040-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53040-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53040-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53040-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53040-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="53040-107">DESCRIPTION</span></span>
<span data-ttu-id="53040-108">A **Remove-AzureRmOperationalInsightsDataSource** parancsmag törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="53040-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="53040-109">Példák</span><span class="sxs-lookup"><span data-stu-id="53040-109">EXAMPLES</span></span>

## <span data-ttu-id="53040-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53040-110">PARAMETERS</span></span>

### <span data-ttu-id="53040-111">-Force</span><span class="sxs-lookup"><span data-stu-id="53040-111">-Force</span></span>
<span data-ttu-id="53040-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="53040-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53040-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53040-113">-Name</span></span>
<span data-ttu-id="53040-114">A törlendő adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53040-114">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="53040-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53040-115">-ResourceGroupName</span></span>
<span data-ttu-id="53040-116">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53040-116">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="53040-117">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="53040-117">-Workspace</span></span>
<span data-ttu-id="53040-118">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="53040-118">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="53040-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53040-119">-WorkspaceName</span></span>
<span data-ttu-id="53040-120">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="53040-120">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="53040-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53040-121">-Confirm</span></span>
<span data-ttu-id="53040-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53040-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53040-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53040-123">-WhatIf</span></span>
<span data-ttu-id="53040-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53040-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53040-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53040-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53040-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53040-126">-DefaultProfile</span></span>
<span data-ttu-id="53040-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53040-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53040-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53040-128">CommonParameters</span></span>
<span data-ttu-id="53040-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53040-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53040-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53040-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53040-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53040-131">INPUTS</span></span>

### <span data-ttu-id="53040-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="53040-132">PSWorkspace</span></span>
<span data-ttu-id="53040-133">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="53040-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="53040-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53040-134">OUTPUTS</span></span>

## <span data-ttu-id="53040-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53040-135">NOTES</span></span>
* <span data-ttu-id="53040-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="53040-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="53040-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53040-137">RELATED LINKS</span></span>

[<span data-ttu-id="53040-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="53040-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="53040-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="53040-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


