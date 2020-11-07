---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4a40b3fd0045a48d6a69c76970b3835ef2d685c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679039"
---
# <span data-ttu-id="3ecab-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3ecab-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="3ecab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ecab-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecab-103">Erőforrás áthelyezése egy másik erőforrás-csoportba vagy előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="3ecab-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ecab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ecab-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ecab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ecab-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecab-106">A **Move-AzureRmResource** parancsmag a meglévő erőforrásokat egy másik erőforráscsoport-csoportba helyezi át.</span><span class="sxs-lookup"><span data-stu-id="3ecab-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="3ecab-107">Az erőforráscsoport más előfizetésben lehet.</span><span class="sxs-lookup"><span data-stu-id="3ecab-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="3ecab-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3ecab-108">EXAMPLES</span></span>

### <span data-ttu-id="3ecab-109">1. példa: erőforrás áthelyezése egy erőforrás-csoportba</span><span class="sxs-lookup"><span data-stu-id="3ecab-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="3ecab-110">Az első parancs az Get-AzureRmResource parancsmag segítségével a ContosoStorageAccount nevű erőforrást kapja, majd az erőforrást a $Resource változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3ecab-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="3ecab-111">A második parancs áthelyezi ezt az erőforrást a ResourceGroup14 nevű erőforráscsoport-csoportba.</span><span class="sxs-lookup"><span data-stu-id="3ecab-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="3ecab-112">A parancs a $Resource **ResourceId** tulajdonságával azonosítja az áthelyezni kívánt erőforrást.</span><span class="sxs-lookup"><span data-stu-id="3ecab-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="3ecab-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ecab-113">PARAMETERS</span></span>

### <span data-ttu-id="3ecab-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3ecab-114">-ApiVersion</span></span>
<span data-ttu-id="3ecab-115">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ecab-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3ecab-116">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="3ecab-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3ecab-117">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ecab-117">-DestinationResourceGroupName</span></span>
<span data-ttu-id="3ecab-118">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a parancsmag az erőforrásokat áthelyezi.</span><span class="sxs-lookup"><span data-stu-id="3ecab-118">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="3ecab-119">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ecab-119">-DestinationSubscriptionId</span></span>
<span data-ttu-id="3ecab-120">Annak az előfizetésnek az AZONOSÍTÓját adja meg, amelybe a parancsmag erőforrásokat helyez.</span><span class="sxs-lookup"><span data-stu-id="3ecab-120">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="3ecab-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3ecab-121">-Force</span></span>
<span data-ttu-id="3ecab-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3ecab-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ecab-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3ecab-123">-InformationAction</span></span>
<span data-ttu-id="3ecab-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3ecab-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3ecab-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3ecab-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ecab-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3ecab-126">Continue</span></span>
- <span data-ttu-id="3ecab-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3ecab-127">Ignore</span></span>
- <span data-ttu-id="3ecab-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3ecab-128">Inquire</span></span>
- <span data-ttu-id="3ecab-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3ecab-129">SilentlyContinue</span></span>
- <span data-ttu-id="3ecab-130">állj</span><span class="sxs-lookup"><span data-stu-id="3ecab-130">Stop</span></span>
- <span data-ttu-id="3ecab-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3ecab-131">Suspend</span></span>

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

### <span data-ttu-id="3ecab-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3ecab-132">-InformationVariable</span></span>
<span data-ttu-id="3ecab-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3ecab-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3ecab-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="3ecab-134">-Pre</span></span>
<span data-ttu-id="3ecab-135">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="3ecab-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3ecab-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ecab-136">-ResourceId</span></span>
<span data-ttu-id="3ecab-137">A parancsmag által áthelyezett erőforrás-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ecab-137">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="3ecab-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ecab-138">-Confirm</span></span>
<span data-ttu-id="3ecab-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ecab-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ecab-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ecab-140">-WhatIf</span></span>
<span data-ttu-id="3ecab-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ecab-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ecab-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ecab-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ecab-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecab-143">-DefaultProfile</span></span>
<span data-ttu-id="3ecab-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ecab-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ecab-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecab-145">CommonParameters</span></span>
<span data-ttu-id="3ecab-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ecab-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecab-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecab-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecab-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ecab-148">INPUTS</span></span>

### <span data-ttu-id="3ecab-149">String []</span><span class="sxs-lookup"><span data-stu-id="3ecab-149">String[]</span></span>
<span data-ttu-id="3ecab-150">A "ResourceId" paraméter értéke a "karakterlánc []" típusú érték beírása a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3ecab-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="3ecab-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ecab-151">OUTPUTS</span></span>

### <span data-ttu-id="3ecab-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ecab-152">System.Boolean</span></span>

## <span data-ttu-id="3ecab-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ecab-153">NOTES</span></span>

## <span data-ttu-id="3ecab-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ecab-154">RELATED LINKS</span></span>

[<span data-ttu-id="3ecab-155">Keresés-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3ecab-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="3ecab-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3ecab-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="3ecab-157">Új – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3ecab-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="3ecab-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3ecab-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="3ecab-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3ecab-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


