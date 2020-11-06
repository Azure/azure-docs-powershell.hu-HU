---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498840"
---
# <span data-ttu-id="45239-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45239-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="45239-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45239-102">SYNOPSIS</span></span>
<span data-ttu-id="45239-103">Egy erőforráscsoport-telepítő és az ahhoz kapcsolódó műveletek eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="45239-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45239-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45239-104">SYNTAX</span></span>

### <span data-ttu-id="45239-105">RemoveByResourceGroupName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45239-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45239-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="45239-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45239-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="45239-107">DESCRIPTION</span></span>
<span data-ttu-id="45239-108">A **Remove-AzureRmResourceGroupDeployment** parancsmag eltávolít egy Azure erőforráscsoport-telepítőt és bármely kapcsolódó műveletet.</span><span class="sxs-lookup"><span data-stu-id="45239-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="45239-109">Példák</span><span class="sxs-lookup"><span data-stu-id="45239-109">EXAMPLES</span></span>

## <span data-ttu-id="45239-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45239-110">PARAMETERS</span></span>

### <span data-ttu-id="45239-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="45239-111">-ApiVersion</span></span>
<span data-ttu-id="45239-112">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="45239-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="45239-113">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="45239-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45239-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45239-114">-DefaultProfile</span></span>
<span data-ttu-id="45239-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45239-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45239-116">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="45239-116">-Id</span></span>
<span data-ttu-id="45239-117">Az eltávolítandó erőforráscsoport-példány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45239-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45239-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45239-118">-Name</span></span>
<span data-ttu-id="45239-119">Az eltávolítandó erőforráscsoport-példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45239-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45239-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="45239-120">-Pre</span></span>
<span data-ttu-id="45239-121">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="45239-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="45239-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45239-122">-ResourceGroupName</span></span>
<span data-ttu-id="45239-123">Az eltávolítandó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45239-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45239-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45239-124">-Confirm</span></span>
<span data-ttu-id="45239-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45239-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45239-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45239-126">-WhatIf</span></span>
<span data-ttu-id="45239-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45239-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45239-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45239-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45239-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45239-129">CommonParameters</span></span>
<span data-ttu-id="45239-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45239-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45239-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45239-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45239-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45239-132">INPUTS</span></span>

### <span data-ttu-id="45239-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="45239-133">None</span></span>
<span data-ttu-id="45239-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="45239-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45239-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45239-135">OUTPUTS</span></span>

### <span data-ttu-id="45239-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45239-136">System.Boolean</span></span>

## <span data-ttu-id="45239-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45239-137">NOTES</span></span>

## <span data-ttu-id="45239-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45239-138">RELATED LINKS</span></span>

[<span data-ttu-id="45239-139">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45239-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="45239-140">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45239-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="45239-141">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45239-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="45239-142">Teszt-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45239-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


