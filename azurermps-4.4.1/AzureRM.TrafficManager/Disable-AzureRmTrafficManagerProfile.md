---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: c3a32c6bab916ad4a63db5e528e00fe3948a1d2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672556"
---
# <span data-ttu-id="35a62-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="35a62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35a62-102">SYNOPSIS</span></span>
<span data-ttu-id="35a62-103">Letiltja a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="35a62-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35a62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35a62-104">SYNTAX</span></span>

### <span data-ttu-id="35a62-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="35a62-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35a62-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="35a62-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a62-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="35a62-107">DESCRIPTION</span></span>
<span data-ttu-id="35a62-108">A **disable-AzureRmTrafficManagerProfile** parancsmag letiltja az Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="35a62-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="35a62-109">Megadhatja a profil objektumát a csővezeték vagy a paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="35a62-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="35a62-110">Azt is megteheti, hogy a *név* és a *ResourceGroupName* paraméterrel megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="35a62-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="35a62-111">Példák</span><span class="sxs-lookup"><span data-stu-id="35a62-111">EXAMPLES</span></span>

### <span data-ttu-id="35a62-112">Példa 1: név szerint megadott profil letiltása</span><span class="sxs-lookup"><span data-stu-id="35a62-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="35a62-113">Ez a parancs letiltja a ContosoProfile nevű ResourceGroup11-profilt.</span><span class="sxs-lookup"><span data-stu-id="35a62-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="35a62-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="35a62-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="35a62-115">2. példa: profil letiltása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="35a62-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="35a62-116">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="35a62-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="35a62-117">Ekkor a parancs átadja a profilt a **AzureRmTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="35a62-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="35a62-118">A parancsmag letiltja a profilt.</span><span class="sxs-lookup"><span data-stu-id="35a62-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="35a62-119">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="35a62-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="35a62-120">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35a62-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="35a62-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35a62-121">PARAMETERS</span></span>

### <span data-ttu-id="35a62-122">-Force</span><span class="sxs-lookup"><span data-stu-id="35a62-122">-Force</span></span>
<span data-ttu-id="35a62-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="35a62-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35a62-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35a62-124">-Name</span></span>
<span data-ttu-id="35a62-125">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="35a62-125">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="35a62-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a62-126">-ResourceGroupName</span></span>
<span data-ttu-id="35a62-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35a62-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="35a62-128">Ez a parancsmag letiltja a forgalomirányító-profilt abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="35a62-128">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="35a62-129">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-129">-TrafficManagerProfile</span></span>
<span data-ttu-id="35a62-130">A letiltani kívánt **TrafficManagerProfile** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="35a62-130">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="35a62-131">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="35a62-131">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="35a62-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35a62-132">-Confirm</span></span>
<span data-ttu-id="35a62-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35a62-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a62-134">-WhatIf</span></span>
<span data-ttu-id="35a62-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35a62-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a62-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35a62-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a62-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-137">-DefaultProfile</span></span>
<span data-ttu-id="35a62-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35a62-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35a62-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a62-139">CommonParameters</span></span>
<span data-ttu-id="35a62-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35a62-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a62-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a62-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a62-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35a62-142">INPUTS</span></span>

### <span data-ttu-id="35a62-143">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="35a62-144">Ez a parancsmag a **TrafficManagerProfile** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="35a62-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="35a62-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35a62-145">OUTPUTS</span></span>

### <span data-ttu-id="35a62-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35a62-146">System.Boolean</span></span>

## <span data-ttu-id="35a62-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35a62-147">NOTES</span></span>

## <span data-ttu-id="35a62-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35a62-148">RELATED LINKS</span></span>

[<span data-ttu-id="35a62-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="35a62-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="35a62-151">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="35a62-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="35a62-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="35a62-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


