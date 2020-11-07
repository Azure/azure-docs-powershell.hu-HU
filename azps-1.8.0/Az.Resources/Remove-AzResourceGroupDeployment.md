---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669332"
---
# <span data-ttu-id="67003-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67003-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="67003-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67003-102">SYNOPSIS</span></span>
<span data-ttu-id="67003-103">Egy erőforráscsoport-telepítő és az ahhoz kapcsolódó műveletek eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="67003-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="67003-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67003-104">SYNTAX</span></span>

### <span data-ttu-id="67003-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67003-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67003-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="67003-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67003-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="67003-107">DESCRIPTION</span></span>
<span data-ttu-id="67003-108">A **Remove-AzResourceGroupDeployment** parancsmag eltávolít egy Azure erőforráscsoport-telepítőt és bármely kapcsolódó műveletet.</span><span class="sxs-lookup"><span data-stu-id="67003-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="67003-109">Példák</span><span class="sxs-lookup"><span data-stu-id="67003-109">EXAMPLES</span></span>

## <span data-ttu-id="67003-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67003-110">PARAMETERS</span></span>

### <span data-ttu-id="67003-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="67003-111">-ApiVersion</span></span>
<span data-ttu-id="67003-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="67003-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="67003-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="67003-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67003-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67003-114">-DefaultProfile</span></span>
<span data-ttu-id="67003-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67003-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67003-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="67003-116">-Id</span></span>
<span data-ttu-id="67003-117">Az eltávolítandó erőforráscsoport-példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="67003-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67003-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67003-118">-Name</span></span>
<span data-ttu-id="67003-119">Az eltávolítandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67003-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67003-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="67003-120">-Pre</span></span>
<span data-ttu-id="67003-121">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="67003-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="67003-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67003-122">-ResourceGroupName</span></span>
<span data-ttu-id="67003-123">Az eltávolítandó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67003-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67003-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="67003-124">-Confirm</span></span>
<span data-ttu-id="67003-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="67003-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67003-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67003-126">-WhatIf</span></span>
<span data-ttu-id="67003-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="67003-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67003-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67003-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67003-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67003-129">CommonParameters</span></span>
<span data-ttu-id="67003-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67003-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67003-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67003-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67003-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67003-132">INPUTS</span></span>

### <span data-ttu-id="67003-133">System. String</span><span class="sxs-lookup"><span data-stu-id="67003-133">System.String</span></span>

## <span data-ttu-id="67003-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67003-134">OUTPUTS</span></span>

### <span data-ttu-id="67003-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67003-135">System.Boolean</span></span>

## <span data-ttu-id="67003-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67003-136">NOTES</span></span>

## <span data-ttu-id="67003-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67003-137">RELATED LINKS</span></span>

[<span data-ttu-id="67003-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67003-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="67003-139">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67003-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="67003-140">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67003-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="67003-141">Teszt-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67003-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


