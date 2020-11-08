---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-Azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: fcee2d5575df49a8f93aa12874c8e658871ca078
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017373"
---
# <span data-ttu-id="ce0ee-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="ce0ee-101">Move-AzResource</span></span>

## <span data-ttu-id="ce0ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0ee-103">Erőforrás áthelyezése egy másik erőforrás-csoportba vagy előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="ce0ee-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="ce0ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce0ee-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce0ee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce0ee-105">DESCRIPTION</span></span>
<span data-ttu-id="ce0ee-106">A **Move-AzResource** parancsmag a meglévő erőforrásokat egy másik erőforráscsoport-csoportba helyezi át.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="ce0ee-107">Az erőforráscsoport más előfizetésben lehet.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="ce0ee-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ce0ee-108">EXAMPLES</span></span>

### <span data-ttu-id="ce0ee-109">1. példa: erőforrás áthelyezése egy erőforrás-csoportba</span><span class="sxs-lookup"><span data-stu-id="ce0ee-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="ce0ee-110">Az első parancs az Get-AzResource parancsmag segítségével a ContosoStorageAccount nevű erőforrást kapja, majd az erőforrást a $Resource változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="ce0ee-111">A második parancs áthelyezi ezt az erőforrást a ResourceGroup14 nevű erőforráscsoport-csoportba.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="ce0ee-112">A parancs a $Resource **ResourceId** tulajdonságával azonosítja az áthelyezni kívánt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="ce0ee-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce0ee-113">PARAMETERS</span></span>

### <span data-ttu-id="ce0ee-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ce0ee-114">-ApiVersion</span></span>
<span data-ttu-id="ce0ee-115">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ce0ee-116">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ce0ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0ee-117">-DefaultProfile</span></span>
<span data-ttu-id="ce0ee-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ce0ee-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0ee-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0ee-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="ce0ee-120">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a parancsmag az erőforrásokat áthelyezi.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="ce0ee-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce0ee-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="ce0ee-122">Annak az előfizetésnek az AZONOSÍTÓját adja meg, amelybe a parancsmag erőforrásokat helyez.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="ce0ee-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ce0ee-123">-Force</span></span>
<span data-ttu-id="ce0ee-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce0ee-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ce0ee-125">-InformationAction</span></span>
<span data-ttu-id="ce0ee-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ce0ee-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ce0ee-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce0ee-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="ce0ee-128">Continue</span></span>
- <span data-ttu-id="ce0ee-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="ce0ee-129">Ignore</span></span>
- <span data-ttu-id="ce0ee-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="ce0ee-130">Inquire</span></span>
- <span data-ttu-id="ce0ee-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ce0ee-131">SilentlyContinue</span></span>
- <span data-ttu-id="ce0ee-132">állj</span><span class="sxs-lookup"><span data-stu-id="ce0ee-132">Stop</span></span>
- <span data-ttu-id="ce0ee-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="ce0ee-133">Suspend</span></span>

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

### <span data-ttu-id="ce0ee-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ce0ee-134">-InformationVariable</span></span>
<span data-ttu-id="ce0ee-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ce0ee-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="ce0ee-136">-Pre</span></span>
<span data-ttu-id="ce0ee-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ce0ee-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce0ee-138">-ResourceId</span></span>
<span data-ttu-id="ce0ee-139">A parancsmag által áthelyezett erőforrás-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="ce0ee-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce0ee-140">-Confirm</span></span>
<span data-ttu-id="ce0ee-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0ee-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0ee-142">-WhatIf</span></span>
<span data-ttu-id="ce0ee-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0ee-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce0ee-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0ee-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0ee-145">CommonParameters</span></span>
<span data-ttu-id="ce0ee-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce0ee-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0ee-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0ee-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0ee-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce0ee-148">INPUTS</span></span>

## <span data-ttu-id="ce0ee-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce0ee-149">OUTPUTS</span></span>

## <span data-ttu-id="ce0ee-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce0ee-150">NOTES</span></span>

## <span data-ttu-id="ce0ee-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce0ee-151">RELATED LINKS</span></span>

[<span data-ttu-id="ce0ee-152">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ce0ee-152">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="ce0ee-153">Új – AzResource</span><span class="sxs-lookup"><span data-stu-id="ce0ee-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="ce0ee-154">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="ce0ee-154">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="ce0ee-155">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="ce0ee-155">Set-AzResource</span></span>](./Set-AzResource.md)


