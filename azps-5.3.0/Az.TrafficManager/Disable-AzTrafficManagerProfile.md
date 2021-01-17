---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382898"
---
# <span data-ttu-id="bc98b-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="bc98b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc98b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc98b-103">Letilt egy Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="bc98b-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="bc98b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bc98b-104">SYNTAX</span></span>

### <span data-ttu-id="bc98b-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="bc98b-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc98b-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="bc98b-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc98b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bc98b-107">DESCRIPTION</span></span>
<span data-ttu-id="bc98b-108">A **Disable-AzTrafficManagerProfile parancsmag** letiltja az Azure Traffic Manager-profilokat.</span><span class="sxs-lookup"><span data-stu-id="bc98b-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="bc98b-109">A profilobjektumot a folyamat használatával vagy paraméterértékként adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="bc98b-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="bc98b-110">Másik lehetőségként a Name és  az *ResourceGroupName* paraméter használatával is megadhatja a profilt.</span><span class="sxs-lookup"><span data-stu-id="bc98b-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="bc98b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bc98b-111">EXAMPLES</span></span>

### <span data-ttu-id="bc98b-112">1. példa: Név szerint megadott profil letiltása</span><span class="sxs-lookup"><span data-stu-id="bc98b-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="bc98b-113">Ez a parancs letiltja a ContosoProfile nevű profilt az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="bc98b-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="bc98b-114">A parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bc98b-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="bc98b-115">2. példa: Profil letiltása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="bc98b-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="bc98b-116">Ez a parancs a ContosoProfile nevű profilt kapja meg az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="bc98b-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="bc98b-117">A parancs ezután átadja a profilt a **Disable-AzTrafficManagerProfile** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="bc98b-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc98b-118">Ez a parancsmag letiltja ezt a profilt.</span><span class="sxs-lookup"><span data-stu-id="bc98b-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="bc98b-119">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc98b-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="bc98b-120">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc98b-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bc98b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc98b-121">PARAMETERS</span></span>

### <span data-ttu-id="bc98b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-122">-DefaultProfile</span></span>
<span data-ttu-id="bc98b-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc98b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc98b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bc98b-124">-Force</span></span>
<span data-ttu-id="bc98b-125">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="bc98b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc98b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bc98b-126">-Name</span></span>
<span data-ttu-id="bc98b-127">A parancsmag által letiltott Traffic Manager-profil neve.</span><span class="sxs-lookup"><span data-stu-id="bc98b-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="bc98b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc98b-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc98b-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc98b-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bc98b-130">Ez a parancsmag letiltja a Traffic Manager-profilt abban a csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc98b-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc98b-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="bc98b-132">Letiltható **TrafficManagerProfile-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="bc98b-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="bc98b-133">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bc98b-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bc98b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc98b-134">-Confirm</span></span>
<span data-ttu-id="bc98b-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bc98b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc98b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc98b-136">-WhatIf</span></span>
<span data-ttu-id="bc98b-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bc98b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc98b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc98b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc98b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc98b-139">CommonParameters</span></span>
<span data-ttu-id="bc98b-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc98b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc98b-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc98b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc98b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc98b-142">INPUTS</span></span>

### <span data-ttu-id="bc98b-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="bc98b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc98b-144">OUTPUTS</span></span>

### <span data-ttu-id="bc98b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc98b-145">System.Boolean</span></span>

## <span data-ttu-id="bc98b-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bc98b-146">NOTES</span></span>

## <span data-ttu-id="bc98b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc98b-147">RELATED LINKS</span></span>

[<span data-ttu-id="bc98b-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="bc98b-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="bc98b-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="bc98b-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="bc98b-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc98b-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


