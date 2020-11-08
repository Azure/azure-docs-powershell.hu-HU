---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194984"
---
# <span data-ttu-id="c5891-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="c5891-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5891-102">SYNOPSIS</span></span>
<span data-ttu-id="c5891-103">Letiltja a Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="c5891-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="c5891-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5891-104">SYNTAX</span></span>

### <span data-ttu-id="c5891-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="c5891-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5891-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="c5891-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5891-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5891-107">DESCRIPTION</span></span>
<span data-ttu-id="c5891-108">A **disable-AzTrafficManagerProfile** parancsmag letiltja az Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="c5891-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c5891-109">Megadhatja a profil objektumát a csővezeték vagy a paraméter értékeként.</span><span class="sxs-lookup"><span data-stu-id="c5891-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="c5891-110">Azt is megteheti, hogy a *név* és a *ResourceGroupName* paraméterrel megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="c5891-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="c5891-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c5891-111">EXAMPLES</span></span>

### <span data-ttu-id="c5891-112">Példa 1: név szerint megadott profil letiltása</span><span class="sxs-lookup"><span data-stu-id="c5891-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c5891-113">Ez a parancs letiltja a ContosoProfile nevű ResourceGroup11-profilt.</span><span class="sxs-lookup"><span data-stu-id="c5891-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c5891-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="c5891-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c5891-115">2. példa: profil letiltása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c5891-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="c5891-116">Ez a parancs a ContosoProfile nevű profilt a ResourceGroup11-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="c5891-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c5891-117">Ekkor a parancs átadja a profilt a **AzTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="c5891-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5891-118">A parancsmag letiltja a profilt.</span><span class="sxs-lookup"><span data-stu-id="c5891-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="c5891-119">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5891-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c5891-120">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5891-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c5891-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5891-121">PARAMETERS</span></span>

### <span data-ttu-id="c5891-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-122">-DefaultProfile</span></span>
<span data-ttu-id="c5891-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5891-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5891-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c5891-124">-Force</span></span>
<span data-ttu-id="c5891-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c5891-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5891-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5891-126">-Name</span></span>
<span data-ttu-id="c5891-127">Annak a forgalomirányító-profilnak a nevét adja meg, amelyre a parancsmag letiltja.</span><span class="sxs-lookup"><span data-stu-id="c5891-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="c5891-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5891-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5891-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5891-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c5891-130">Ez a parancsmag letiltja a forgalomirányító-profilt abban a csoportban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c5891-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5891-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="c5891-132">A letiltani kívánt **TrafficManagerProfile** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5891-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="c5891-133">**TrafficManagerProfile** objektum beolvasásához használja az Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c5891-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c5891-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5891-134">-Confirm</span></span>
<span data-ttu-id="c5891-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5891-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5891-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5891-136">-WhatIf</span></span>
<span data-ttu-id="c5891-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5891-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5891-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5891-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5891-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5891-139">CommonParameters</span></span>
<span data-ttu-id="c5891-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5891-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5891-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5891-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5891-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5891-142">INPUTS</span></span>

### <span data-ttu-id="c5891-143">Microsoft. Azure. Command. TrafficManager. models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c5891-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5891-144">OUTPUTS</span></span>

### <span data-ttu-id="c5891-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5891-145">System.Boolean</span></span>

## <span data-ttu-id="c5891-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5891-146">NOTES</span></span>

## <span data-ttu-id="c5891-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5891-147">RELATED LINKS</span></span>

[<span data-ttu-id="c5891-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5891-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5891-150">Új – AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5891-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="c5891-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5891-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

