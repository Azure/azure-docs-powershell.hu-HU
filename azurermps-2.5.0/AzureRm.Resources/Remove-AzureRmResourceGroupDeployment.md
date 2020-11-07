---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: bfe0bad0104708e635b49f02cfb1eecd2474ea5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850537"
---
# <span data-ttu-id="46671-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46671-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="46671-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46671-102">SYNOPSIS</span></span>
<span data-ttu-id="46671-103">Egy erőforráscsoport-telepítő és az ahhoz kapcsolódó műveletek eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="46671-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46671-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46671-104">SYNTAX</span></span>

### <span data-ttu-id="46671-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46671-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46671-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="46671-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46671-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="46671-107">DESCRIPTION</span></span>
<span data-ttu-id="46671-108">A **Remove-AzureRmResourceGroupDeployment** parancsmag eltávolít egy Azure erőforráscsoport-telepítőt és bármely kapcsolódó műveletet.</span><span class="sxs-lookup"><span data-stu-id="46671-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="46671-109">Példák</span><span class="sxs-lookup"><span data-stu-id="46671-109">EXAMPLES</span></span>

## <span data-ttu-id="46671-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46671-110">PARAMETERS</span></span>

### <span data-ttu-id="46671-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="46671-111">-ApiVersion</span></span>
<span data-ttu-id="46671-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="46671-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="46671-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="46671-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="46671-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46671-114">-DefaultProfile</span></span>
<span data-ttu-id="46671-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="46671-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46671-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="46671-116">-Id</span></span>
<span data-ttu-id="46671-117">Az eltávolítandó erőforráscsoport-példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46671-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="46671-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46671-118">-Name</span></span>
<span data-ttu-id="46671-119">Az eltávolítandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46671-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46671-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="46671-120">-Pre</span></span>
<span data-ttu-id="46671-121">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="46671-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="46671-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46671-122">-ResourceGroupName</span></span>
<span data-ttu-id="46671-123">Az eltávolítandó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46671-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46671-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46671-124">-Confirm</span></span>
<span data-ttu-id="46671-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46671-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46671-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46671-126">-WhatIf</span></span>
<span data-ttu-id="46671-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46671-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46671-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46671-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46671-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46671-129">CommonParameters</span></span>
<span data-ttu-id="46671-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46671-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46671-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46671-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46671-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46671-132">INPUTS</span></span>

### <span data-ttu-id="46671-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="46671-133">None</span></span>

## <span data-ttu-id="46671-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46671-134">OUTPUTS</span></span>

## <span data-ttu-id="46671-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46671-135">NOTES</span></span>

## <span data-ttu-id="46671-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46671-136">RELATED LINKS</span></span>

[<span data-ttu-id="46671-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46671-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="46671-138">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46671-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="46671-139">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46671-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="46671-140">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46671-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


