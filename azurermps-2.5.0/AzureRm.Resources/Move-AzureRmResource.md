---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
ms.openlocfilehash: 4f50aea600fe930de62a65d566b6a6ec723fc8de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849905"
---
# <span data-ttu-id="ec825-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ec825-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="ec825-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec825-102">SYNOPSIS</span></span>
<span data-ttu-id="ec825-103">Erőforrás áthelyezése egy másik erőforrás-csoportba vagy előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="ec825-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec825-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec825-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec825-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec825-105">DESCRIPTION</span></span>
<span data-ttu-id="ec825-106">A **Move-AzureRmResource** parancsmag a meglévő erőforrásokat egy másik erőforráscsoport-csoportba helyezi át.</span><span class="sxs-lookup"><span data-stu-id="ec825-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="ec825-107">Az erőforráscsoport más előfizetésben lehet.</span><span class="sxs-lookup"><span data-stu-id="ec825-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="ec825-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ec825-108">EXAMPLES</span></span>

### <span data-ttu-id="ec825-109">1. példa: erőforrás áthelyezése egy erőforrás-csoportba</span><span class="sxs-lookup"><span data-stu-id="ec825-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="ec825-110">Az első parancs az Get-AzureRmResource parancsmag segítségével a ContosoStorageAccount nevű erőforrást kapja, majd az erőforrást a $Resource változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ec825-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="ec825-111">A második parancs áthelyezi ezt az erőforrást a ResourceGroup14 nevű erőforráscsoport-csoportba.</span><span class="sxs-lookup"><span data-stu-id="ec825-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="ec825-112">A parancs a $Resource **ResourceId** tulajdonságával azonosítja az áthelyezni kívánt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="ec825-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="ec825-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec825-113">PARAMETERS</span></span>

### <span data-ttu-id="ec825-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ec825-114">-ApiVersion</span></span>
<span data-ttu-id="ec825-115">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec825-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ec825-116">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ec825-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ec825-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec825-117">-DefaultProfile</span></span>
<span data-ttu-id="ec825-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ec825-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec825-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec825-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="ec825-120">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a parancsmag az erőforrásokat áthelyezi.</span><span class="sxs-lookup"><span data-stu-id="ec825-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec825-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec825-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="ec825-122">Annak az előfizetésnek az AZONOSÍTÓját adja meg, amelybe a parancsmag erőforrásokat helyez.</span><span class="sxs-lookup"><span data-stu-id="ec825-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec825-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ec825-123">-Force</span></span>
<span data-ttu-id="ec825-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ec825-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec825-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ec825-125">-InformationAction</span></span>
<span data-ttu-id="ec825-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ec825-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ec825-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ec825-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec825-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ec825-128">Continue</span></span>
- <span data-ttu-id="ec825-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ec825-129">Ignore</span></span>
- <span data-ttu-id="ec825-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ec825-130">Inquire</span></span>
- <span data-ttu-id="ec825-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ec825-131">SilentlyContinue</span></span>
- <span data-ttu-id="ec825-132">állj</span><span class="sxs-lookup"><span data-stu-id="ec825-132">Stop</span></span>
- <span data-ttu-id="ec825-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ec825-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec825-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ec825-134">-InformationVariable</span></span>
<span data-ttu-id="ec825-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ec825-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec825-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="ec825-136">-Pre</span></span>
<span data-ttu-id="ec825-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ec825-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ec825-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec825-138">-ResourceId</span></span>
<span data-ttu-id="ec825-139">A parancsmag által áthelyezett erőforrás-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec825-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec825-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec825-140">-Confirm</span></span>
<span data-ttu-id="ec825-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec825-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec825-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec825-142">-WhatIf</span></span>
<span data-ttu-id="ec825-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec825-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec825-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec825-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec825-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec825-145">CommonParameters</span></span>
<span data-ttu-id="ec825-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec825-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec825-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec825-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec825-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec825-148">INPUTS</span></span>

## <span data-ttu-id="ec825-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec825-149">OUTPUTS</span></span>

## <span data-ttu-id="ec825-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec825-150">NOTES</span></span>

## <span data-ttu-id="ec825-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec825-151">RELATED LINKS</span></span>



[<span data-ttu-id="ec825-152">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ec825-152">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ec825-153">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ec825-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ec825-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ec825-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="ec825-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ec825-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


