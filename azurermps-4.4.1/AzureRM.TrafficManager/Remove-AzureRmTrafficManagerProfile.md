---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 01a82084ddcea5fc3a5a3c412b7b6ea20dfcaa02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673081"
---
# <span data-ttu-id="898b4-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="898b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="898b4-102">SYNOPSIS</span></span>
<span data-ttu-id="898b4-103">Adatforgalom-kezelő profil törlése</span><span class="sxs-lookup"><span data-stu-id="898b4-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="898b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="898b4-104">SYNTAX</span></span>

### <span data-ttu-id="898b4-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="898b4-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="898b4-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="898b4-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="898b4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="898b4-107">DESCRIPTION</span></span>
<span data-ttu-id="898b4-108">A **Remove-AzureRmTrafficManagerProfile** parancsmag egy Azure Traffic Manager-profilt töröl.</span><span class="sxs-lookup"><span data-stu-id="898b4-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="898b4-109">A *név* és a *ResourceGroupName* paraméter használatával adja meg a törlendő profilt.</span><span class="sxs-lookup"><span data-stu-id="898b4-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="898b4-110">Másik lehetőségként megadhat egy **TrafficManagerProfile** -objektumot a *TrafficManagerProfile* paraméterrel, vagy használhatja a csővezetéket is.</span><span class="sxs-lookup"><span data-stu-id="898b4-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="898b4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="898b4-111">EXAMPLES</span></span>

### <span data-ttu-id="898b4-112">Példa 1: név szerint megadott profil törlése</span><span class="sxs-lookup"><span data-stu-id="898b4-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="898b4-113">Ez a parancs törli a ContosoProfile nevű profilt a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="898b4-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="898b4-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="898b4-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="898b4-115">2. példa: profil törlése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="898b4-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="898b4-116">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="898b4-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="898b4-117">Ekkor a parancs átadja a profilt a **Remove-AzureRmTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="898b4-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="898b4-118">E parancsmag törli azt a profilt.</span><span class="sxs-lookup"><span data-stu-id="898b4-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="898b4-119">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="898b4-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="898b4-120">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="898b4-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="898b4-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="898b4-121">PARAMETERS</span></span>

### <span data-ttu-id="898b4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="898b4-122">-Force</span></span>
<span data-ttu-id="898b4-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="898b4-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="898b4-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="898b4-124">-Name</span></span>
<span data-ttu-id="898b4-125">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="898b4-125">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="898b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="898b4-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="898b4-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="898b4-128">Ez a parancsmag törli a forgalomirányító-profilt abban a csoportban, amely a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="898b4-128">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="898b4-129">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-129">-TrafficManagerProfile</span></span>
<span data-ttu-id="898b4-130">A törlendő **TrafficManagerProfile** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="898b4-130">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="898b4-131">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="898b4-131">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="898b4-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="898b4-132">-Confirm</span></span>
<span data-ttu-id="898b4-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="898b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="898b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="898b4-134">-WhatIf</span></span>
<span data-ttu-id="898b4-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="898b4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="898b4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="898b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="898b4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-137">-DefaultProfile</span></span>
<span data-ttu-id="898b4-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="898b4-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="898b4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898b4-139">CommonParameters</span></span>
<span data-ttu-id="898b4-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="898b4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898b4-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="898b4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898b4-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="898b4-142">INPUTS</span></span>

### <span data-ttu-id="898b4-143">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="898b4-144">Ez a parancsmag a **TrafficManagerProfile** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="898b4-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="898b4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="898b4-145">OUTPUTS</span></span>

### <span data-ttu-id="898b4-146">Logikai</span><span class="sxs-lookup"><span data-stu-id="898b4-146">Boolean</span></span>
<span data-ttu-id="898b4-147">Ez a parancsmag a $True értékének értékét számítja ki, ha az nem sikerül, vagy ha a törlés sikertelen, az $False értéke.</span><span class="sxs-lookup"><span data-stu-id="898b4-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="898b4-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="898b4-148">NOTES</span></span>

## <span data-ttu-id="898b4-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="898b4-149">RELATED LINKS</span></span>

[<span data-ttu-id="898b4-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="898b4-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="898b4-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="898b4-153">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="898b4-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="898b4-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


