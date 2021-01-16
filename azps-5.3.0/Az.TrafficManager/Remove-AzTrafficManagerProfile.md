---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375814"
---
# <span data-ttu-id="4ff43-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="4ff43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ff43-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff43-103">Törli a Forgalomkezelő-profilt.</span><span class="sxs-lookup"><span data-stu-id="4ff43-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="4ff43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ff43-104">SYNTAX</span></span>

### <span data-ttu-id="4ff43-105">Mezők</span><span class="sxs-lookup"><span data-stu-id="4ff43-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff43-106">Objektum</span><span class="sxs-lookup"><span data-stu-id="4ff43-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff43-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ff43-107">DESCRIPTION</span></span>
<span data-ttu-id="4ff43-108">A **Remove-AzTrafficManagerProfile** parancsmag töröl egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="4ff43-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="4ff43-109">Adja meg a törölni kívánt profilt a *Name* és *az ResourceGroupName* paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="4ff43-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4ff43-110">Másik lehetőségként megadhatja a **TrafficManagerProfile** objektumot a *TrafficManagerProfile* paraméterrel, vagy használhatja a folyamatot.</span><span class="sxs-lookup"><span data-stu-id="4ff43-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="4ff43-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ff43-111">EXAMPLES</span></span>

### <span data-ttu-id="4ff43-112">1. példa: Név szerint megadott profil törlése</span><span class="sxs-lookup"><span data-stu-id="4ff43-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4ff43-113">Ez a parancs törli a ContosoProfile nevű profilt az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="4ff43-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="4ff43-114">A parancs megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ff43-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="4ff43-115">2. példa: Profil törlése a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="4ff43-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="4ff43-116">Ez a parancs a ContosoProfile nevű profilt kapja meg az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="4ff43-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="4ff43-117">A parancs ezután átadja a profilt a **Remove-AzTrafficManagerProfile** parancsmagnak a folyamat műveleti operátorával.</span><span class="sxs-lookup"><span data-stu-id="4ff43-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4ff43-118">Ez a parancsmag törli ezt a profilt.</span><span class="sxs-lookup"><span data-stu-id="4ff43-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="4ff43-119">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff43-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4ff43-120">Ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ff43-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4ff43-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ff43-121">PARAMETERS</span></span>

### <span data-ttu-id="4ff43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-122">-DefaultProfile</span></span>
<span data-ttu-id="4ff43-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ff43-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ff43-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4ff43-124">-Force</span></span>
<span data-ttu-id="4ff43-125">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4ff43-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ff43-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4ff43-126">-Name</span></span>
<span data-ttu-id="4ff43-127">Annak a Traffic Manager-profilnak a nevét adja meg, amelyből a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="4ff43-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="4ff43-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff43-128">-ResourceGroupName</span></span>
<span data-ttu-id="4ff43-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff43-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4ff43-130">Ez a parancsmag törli a Traffic Manager-profilt abban a csoportban, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff43-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ff43-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="4ff43-132">A **törölni kívánt TrafficManagerProfile** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ff43-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="4ff43-133">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4ff43-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4ff43-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ff43-134">-Confirm</span></span>
<span data-ttu-id="4ff43-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4ff43-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff43-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff43-136">-WhatIf</span></span>
<span data-ttu-id="4ff43-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4ff43-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ff43-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ff43-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff43-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff43-139">CommonParameters</span></span>
<span data-ttu-id="4ff43-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff43-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff43-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ff43-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff43-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ff43-142">INPUTS</span></span>

### <span data-ttu-id="4ff43-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4ff43-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ff43-144">OUTPUTS</span></span>

### <span data-ttu-id="4ff43-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ff43-145">System.Boolean</span></span>

## <span data-ttu-id="4ff43-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ff43-146">NOTES</span></span>

## <span data-ttu-id="4ff43-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ff43-147">RELATED LINKS</span></span>

[<span data-ttu-id="4ff43-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ff43-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ff43-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ff43-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="4ff43-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ff43-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


