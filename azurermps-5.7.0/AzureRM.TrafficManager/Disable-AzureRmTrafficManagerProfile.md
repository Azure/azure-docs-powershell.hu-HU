---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 99bff202a67dcc0db6109f3622188e10d250c573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673202"
---
# <span data-ttu-id="7d2fc-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="7d2fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2fc-103">Letiltja a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d2fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d2fc-104">SYNTAX</span></span>

### <span data-ttu-id="7d2fc-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="7d2fc-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2fc-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="7d2fc-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2fc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d2fc-107">DESCRIPTION</span></span>
<span data-ttu-id="7d2fc-108">A **disable-AzureRmTrafficManagerProfile** parancsmag letiltja az Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7d2fc-109">Megadhatja a profil objektumát a csővezeték vagy a paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="7d2fc-110">Azt is megteheti, hogy a *név* és a *ResourceGroupName* paraméterrel megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="7d2fc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7d2fc-111">EXAMPLES</span></span>

### <span data-ttu-id="7d2fc-112">Példa 1: név szerint megadott profil letiltása</span><span class="sxs-lookup"><span data-stu-id="7d2fc-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7d2fc-113">Ez a parancs letiltja a ContosoProfile nevű ResourceGroup11-profilt.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7d2fc-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7d2fc-115">2. példa: profil letiltása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="7d2fc-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="7d2fc-116">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7d2fc-117">Ekkor a parancs átadja a profilt a **AzureRmTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7d2fc-118">A parancsmag letiltja a profilt.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="7d2fc-119">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7d2fc-120">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7d2fc-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d2fc-121">PARAMETERS</span></span>

### <span data-ttu-id="7d2fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-122">-DefaultProfile</span></span>
<span data-ttu-id="7d2fc-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d2fc-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7d2fc-124">-Force</span></span>
<span data-ttu-id="7d2fc-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d2fc-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7d2fc-126">-Name</span></span>
<span data-ttu-id="7d2fc-127">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="7d2fc-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7d2fc-130">Ez a parancsmag letiltja a forgalomirányító-profilt abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2fc-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="7d2fc-132">A letiltani kívánt **TrafficManagerProfile** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="7d2fc-133">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzureRmTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2fc-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d2fc-134">-Confirm</span></span>
<span data-ttu-id="7d2fc-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2fc-136">-WhatIf</span></span>
<span data-ttu-id="7d2fc-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d2fc-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2fc-139">CommonParameters</span></span>
<span data-ttu-id="7d2fc-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d2fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2fc-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2fc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2fc-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d2fc-142">INPUTS</span></span>

### <span data-ttu-id="7d2fc-143">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="7d2fc-144">Ez a parancsmag a **TrafficManagerProfile** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="7d2fc-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d2fc-145">OUTPUTS</span></span>

### <span data-ttu-id="7d2fc-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d2fc-146">System.Boolean</span></span>

## <span data-ttu-id="7d2fc-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d2fc-147">NOTES</span></span>

## <span data-ttu-id="7d2fc-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d2fc-148">RELATED LINKS</span></span>

[<span data-ttu-id="7d2fc-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d2fc-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d2fc-151">Új – AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d2fc-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="7d2fc-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d2fc-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


