---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 8025c68c7fcaf2e7757cc81718636785bd62a19b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850858"
---
# <span data-ttu-id="04a0c-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04a0c-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="04a0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="04a0c-103">Egy automéretarányos beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04a0c-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04a0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04a0c-104">SYNTAX</span></span>

### <span data-ttu-id="04a0c-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04a0c-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04a0c-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04a0c-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a0c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="04a0c-107">DESCRIPTION</span></span>
<span data-ttu-id="04a0c-108">Az **Add-AzureRmAutoscaleSetting** parancsmag automéretarányos beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="04a0c-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="04a0c-109">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="04a0c-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="04a0c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="04a0c-110">EXAMPLES</span></span>

### <span data-ttu-id="04a0c-111">Példa 1: automéretarányos beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="04a0c-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="04a0c-112">Az első két parancs New-AzureRmAutoscaleRule segítségével két automéretarányos szabályt hozhat létre, $Rule 1 és a $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="04a0c-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="04a0c-113">A harmadik és a negyedik parancs New-AzureRmAutoscaleProfile segítségével hozzon létre automéretarányos profilokat, $Profile 1 és $Profile 2 $Rule 1 és $Rule 2 segítségével.</span><span class="sxs-lookup"><span data-stu-id="04a0c-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="04a0c-114">A végleges parancs a $Profile 1 és a $Profile 2 profilok segítségével automatikusan létrehoz egy automéretarányos beállítást.</span><span class="sxs-lookup"><span data-stu-id="04a0c-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="04a0c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04a0c-115">PARAMETERS</span></span>

### <span data-ttu-id="04a0c-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="04a0c-116">-AutoscaleProfile</span></span>
<span data-ttu-id="04a0c-117">Itt adhatja meg az automéretarány beállításához hozzáadni kívánt profilok listáját, vagy $Null a nincs profil hozzáadása lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="04a0c-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="04a0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a0c-118">-DefaultProfile</span></span>
<span data-ttu-id="04a0c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="04a0c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04a0c-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="04a0c-120">-DisableSetting</span></span>
<span data-ttu-id="04a0c-121">A meglévő automéretarány-beállítás letiltása.</span><span class="sxs-lookup"><span data-stu-id="04a0c-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="04a0c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04a0c-122">-InputObject</span></span>
<span data-ttu-id="04a0c-123">Egy AutoscaleSetting teljes specifikációja</span><span class="sxs-lookup"><span data-stu-id="04a0c-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="04a0c-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="04a0c-124">-Location</span></span>
<span data-ttu-id="04a0c-125">Az automéretarány beállítás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04a0c-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="04a0c-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="04a0c-126">-Name</span></span>
<span data-ttu-id="04a0c-127">A létrehozandó méretezési beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04a0c-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="04a0c-128">-Értesítés</span><span class="sxs-lookup"><span data-stu-id="04a0c-128">-Notification</span></span>
<span data-ttu-id="04a0c-129">A pontosvesszővel tagolt értesítések listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="04a0c-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="04a0c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a0c-130">-ResourceGroupName</span></span>
<span data-ttu-id="04a0c-131">Az automéretarány beállítással társított erőforrás erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04a0c-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="04a0c-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="04a0c-132">-TargetResourceId</span></span>
<span data-ttu-id="04a0c-133">Az erőforrás AZONOSÍTÓját adja meg az autoscale értékhez.</span><span class="sxs-lookup"><span data-stu-id="04a0c-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="04a0c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="04a0c-134">-Confirm</span></span>
<span data-ttu-id="04a0c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="04a0c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a0c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a0c-136">-WhatIf</span></span>
<span data-ttu-id="04a0c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="04a0c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04a0c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04a0c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a0c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a0c-139">CommonParameters</span></span>
<span data-ttu-id="04a0c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04a0c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a0c-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a0c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a0c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04a0c-142">INPUTS</span></span>

### <span data-ttu-id="04a0c-143">Microsoft. Azure. commands. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04a0c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="04a0c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="04a0c-144">System.String</span></span>

### <span data-ttu-id="04a0c-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="04a0c-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="04a0c-146">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. AutoscaleProfile, Microsoft. Azure. commands. ininsights, Version = 5.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="04a0c-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="04a0c-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. AutoscaleNotification, Microsoft. Azure. commands. ininsights, Version = 5.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="04a0c-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="04a0c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04a0c-148">OUTPUTS</span></span>

### <span data-ttu-id="04a0c-149">Microsoft. Azure. commands. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="04a0c-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="04a0c-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04a0c-150">NOTES</span></span>

## <span data-ttu-id="04a0c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04a0c-151">RELATED LINKS</span></span>

[<span data-ttu-id="04a0c-152">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04a0c-152">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="04a0c-153">Új – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="04a0c-153">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="04a0c-154">Új – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="04a0c-154">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="04a0c-155">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04a0c-155">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


