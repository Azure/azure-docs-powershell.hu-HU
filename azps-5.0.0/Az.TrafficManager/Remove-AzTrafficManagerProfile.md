---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194150"
---
# <span data-ttu-id="8f878-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="8f878-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f878-102">SYNOPSIS</span></span>
<span data-ttu-id="8f878-103">Adatforgalom-kezelő profil törlése</span><span class="sxs-lookup"><span data-stu-id="8f878-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="8f878-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f878-104">SYNTAX</span></span>

### <span data-ttu-id="8f878-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="8f878-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f878-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="8f878-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f878-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f878-107">DESCRIPTION</span></span>
<span data-ttu-id="8f878-108">A **Remove-AzTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt töröl.</span><span class="sxs-lookup"><span data-stu-id="8f878-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8f878-109">A *név* és a *ResourceGroupName* paraméter használatával adja meg a törlendő profilt.</span><span class="sxs-lookup"><span data-stu-id="8f878-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8f878-110">Másik lehetőségként megadhat egy **TrafficManagerProfile** -objektumot a *TrafficManagerProfile* paraméterrel, vagy használhatja a csővezetéket is.</span><span class="sxs-lookup"><span data-stu-id="8f878-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="8f878-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8f878-111">EXAMPLES</span></span>

### <span data-ttu-id="8f878-112">Példa 1: név szerint megadott profil törlése</span><span class="sxs-lookup"><span data-stu-id="8f878-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8f878-113">Ez a parancs törli a ContosoProfile nevű profilt a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8f878-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8f878-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="8f878-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8f878-115">2. példa: profil törlése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="8f878-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="8f878-116">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="8f878-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8f878-117">Ekkor a parancs átadja a profilt a **Remove-AzTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="8f878-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8f878-118">E parancsmag törli azt a profilt.</span><span class="sxs-lookup"><span data-stu-id="8f878-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="8f878-119">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f878-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8f878-120">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f878-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8f878-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f878-121">PARAMETERS</span></span>

### <span data-ttu-id="8f878-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-122">-DefaultProfile</span></span>
<span data-ttu-id="8f878-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f878-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f878-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8f878-124">-Force</span></span>
<span data-ttu-id="8f878-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8f878-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f878-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f878-126">-Name</span></span>
<span data-ttu-id="8f878-127">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="8f878-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f878-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f878-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f878-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f878-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8f878-130">Ez a parancsmag törli a forgalomirányító-profilt abban a csoportban, amely a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f878-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f878-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="8f878-132">A törlendő **TrafficManagerProfile** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f878-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="8f878-133">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8f878-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f878-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f878-134">-Confirm</span></span>
<span data-ttu-id="8f878-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f878-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f878-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f878-136">-WhatIf</span></span>
<span data-ttu-id="8f878-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f878-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f878-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f878-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f878-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f878-139">CommonParameters</span></span>
<span data-ttu-id="8f878-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f878-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f878-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f878-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f878-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f878-142">INPUTS</span></span>

### <span data-ttu-id="8f878-143">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8f878-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f878-144">OUTPUTS</span></span>

### <span data-ttu-id="8f878-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f878-145">System.Boolean</span></span>

## <span data-ttu-id="8f878-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f878-146">NOTES</span></span>

## <span data-ttu-id="8f878-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f878-147">RELATED LINKS</span></span>

[<span data-ttu-id="8f878-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="8f878-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="8f878-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8f878-151">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="8f878-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f878-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

