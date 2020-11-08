---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b2f7410f45a5b60a768d22fe7e66b7d8c1e4ad94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187293"
---
# <span data-ttu-id="f6eea-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f6eea-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="f6eea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6eea-102">SYNOPSIS</span></span>
<span data-ttu-id="f6eea-103">Egy automéretarányos beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6eea-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="f6eea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6eea-104">SYNTAX</span></span>

### <span data-ttu-id="f6eea-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f6eea-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6eea-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f6eea-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6eea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6eea-107">DESCRIPTION</span></span>
<span data-ttu-id="f6eea-108">Az **Add-AzAutoscaleSetting** parancsmag automéretarányos beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6eea-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="f6eea-109">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="f6eea-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f6eea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f6eea-110">EXAMPLES</span></span>

### <span data-ttu-id="f6eea-111">Példa 1: automéretarányos beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="f6eea-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="f6eea-112">Az első két parancs a [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) segítségével két automéretarányos szabályt hoz létre, $Rule 1 és $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="f6eea-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="f6eea-113">A harmadik és a negyedik parancs a [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) használatával hozzon létre automéretarányos profilokat, $Profile 1 és $Profile 2 $Rule 1 és $Rule 2 segítségével.</span><span class="sxs-lookup"><span data-stu-id="f6eea-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="f6eea-114">A végleges parancs a $Profile 1 és a $Profile 2 profilok segítségével automatikusan létrehoz egy automéretarányos beállítást.</span><span class="sxs-lookup"><span data-stu-id="f6eea-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="f6eea-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6eea-115">PARAMETERS</span></span>

### <span data-ttu-id="f6eea-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f6eea-116">-AutoscaleProfile</span></span>
<span data-ttu-id="f6eea-117">Itt adhatja meg az automéretarány beállításához hozzáadni kívánt profilok listáját, vagy $Null a nincs profil hozzáadása lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f6eea-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6eea-118">-DefaultProfile</span></span>
<span data-ttu-id="f6eea-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f6eea-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6eea-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="f6eea-120">-DisableSetting</span></span>
<span data-ttu-id="f6eea-121">A meglévő automéretarány-beállítás letiltása.</span><span class="sxs-lookup"><span data-stu-id="f6eea-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6eea-122">-InputObject</span></span>
<span data-ttu-id="f6eea-123">Egy AutoscaleSetting teljes specifikációja</span><span class="sxs-lookup"><span data-stu-id="f6eea-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="f6eea-124">-Location</span></span>
<span data-ttu-id="f6eea-125">Az automéretarány beállítás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6eea-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6eea-126">-Name</span></span>
<span data-ttu-id="f6eea-127">A létrehozandó méretezési beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6eea-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-128">-Értesítés</span><span class="sxs-lookup"><span data-stu-id="f6eea-128">-Notification</span></span>
<span data-ttu-id="f6eea-129">A pontosvesszővel tagolt értesítések listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6eea-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6eea-130">-ResourceGroupName</span></span>
<span data-ttu-id="f6eea-131">Az automéretarány beállítással társított erőforrás erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6eea-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f6eea-132">-TargetResourceId</span></span>
<span data-ttu-id="f6eea-133">Az erőforrás AZONOSÍTÓját adja meg az autoscale értékhez.</span><span class="sxs-lookup"><span data-stu-id="f6eea-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6eea-134">-Confirm</span></span>
<span data-ttu-id="f6eea-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6eea-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6eea-136">-WhatIf</span></span>
<span data-ttu-id="f6eea-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6eea-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6eea-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6eea-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6eea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6eea-139">CommonParameters</span></span>
<span data-ttu-id="f6eea-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6eea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6eea-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f6eea-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6eea-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6eea-142">INPUTS</span></span>

### <span data-ttu-id="f6eea-143">Microsoft. Azure. commands. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f6eea-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="f6eea-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f6eea-144">System.String</span></span>

### <span data-ttu-id="f6eea-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6eea-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f6eea-146">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. AutoscaleProfile, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f6eea-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f6eea-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. AutoscaleNotification, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f6eea-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f6eea-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6eea-148">OUTPUTS</span></span>

### <span data-ttu-id="f6eea-149">Microsoft. Azure. commands. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f6eea-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="f6eea-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6eea-150">NOTES</span></span>

## <span data-ttu-id="f6eea-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6eea-151">RELATED LINKS</span></span>

[<span data-ttu-id="f6eea-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f6eea-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="f6eea-153">Új – AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f6eea-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="f6eea-154">Új – AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="f6eea-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="f6eea-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f6eea-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


