---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680543"
---
# <span data-ttu-id="99307-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="99307-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="99307-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99307-102">SYNOPSIS</span></span>
<span data-ttu-id="99307-103">Egy automéretarányos beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99307-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99307-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99307-104">SYNTAX</span></span>

### <span data-ttu-id="99307-105">Add-AzureRmAutoscaleSetting parancsmag paraméterei a frissítési szemantikai adatokban</span><span class="sxs-lookup"><span data-stu-id="99307-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99307-106">Add-AzureRmAutoscaleSetting parancsmag paraméterei a szemantika létrehozása során</span><span class="sxs-lookup"><span data-stu-id="99307-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99307-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="99307-107">DESCRIPTION</span></span>
<span data-ttu-id="99307-108">Az **Add-AzureRmAutoscaleSetting** parancsmag automéretarányos beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="99307-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="99307-109">Példák</span><span class="sxs-lookup"><span data-stu-id="99307-109">EXAMPLES</span></span>

### <span data-ttu-id="99307-110">Példa 1: automéretarányos beállítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="99307-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="99307-111">Az első két parancs New-AzureRmAutoscaleRule segítségével két automéretarányos szabályt hozhat létre, $Rule 1 és a $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="99307-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="99307-112">A harmadik és a negyedik parancs New-AzureRmAutoscaleProfile segítségével hozzon létre automéretarányos profilokat, $Profile 1 és $Profile 2 $Rule 1 és $Rule 2 segítségével.</span><span class="sxs-lookup"><span data-stu-id="99307-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="99307-113">A végleges parancs a $Profile 1 és a $Profile 2 profilok segítségével automatikusan létrehoz egy automéretarányos beállítást.</span><span class="sxs-lookup"><span data-stu-id="99307-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="99307-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99307-114">PARAMETERS</span></span>

### <span data-ttu-id="99307-115">-AutoscaleProfiles</span><span class="sxs-lookup"><span data-stu-id="99307-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="99307-116">Itt adhatja meg az automéretarány beállításához hozzáadni kívánt profilok listáját, vagy $Null a nincs profil hozzáadása lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="99307-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="99307-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="99307-117">-DisableSetting</span></span>
<span data-ttu-id="99307-118">A meglévő automéretarány-beállítás letiltása.</span><span class="sxs-lookup"><span data-stu-id="99307-118">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="99307-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="99307-119">-Location</span></span>
<span data-ttu-id="99307-120">Az automéretarány beállítás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99307-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99307-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99307-121">-Name</span></span>
<span data-ttu-id="99307-122">A létrehozandó méretezési beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99307-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99307-123">– Értesítések</span><span class="sxs-lookup"><span data-stu-id="99307-123">-Notifications</span></span>
<span data-ttu-id="99307-124">A pontosvesszővel tagolt értesítések listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99307-124">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="99307-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="99307-125">-ResourceGroup</span></span>
<span data-ttu-id="99307-126">Az automéretarány beállítással társított erőforrás erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99307-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99307-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="99307-127">-SettingSpec</span></span>
<span data-ttu-id="99307-128">Egy **AutoscaleSetting** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="99307-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="99307-129">A Get-AzureRmAutoscaleSetting parancsmaggal **AutoscaleSetting** objektumot hozhat létre, vagy egy Windows PowerShell-parancsfájlban létrehozhatja az egyiket.</span><span class="sxs-lookup"><span data-stu-id="99307-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99307-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="99307-130">-TargetResourceId</span></span>
<span data-ttu-id="99307-131">Az erőforrás AZONOSÍTÓját adja meg az autoscale értékhez.</span><span class="sxs-lookup"><span data-stu-id="99307-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99307-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99307-132">-DefaultProfile</span></span>
<span data-ttu-id="99307-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99307-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99307-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99307-134">CommonParameters</span></span>
<span data-ttu-id="99307-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99307-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99307-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99307-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99307-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99307-137">INPUTS</span></span>

## <span data-ttu-id="99307-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99307-138">OUTPUTS</span></span>

### <span data-ttu-id="99307-139">Microsoft. Azure. commands. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="99307-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="99307-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99307-140">NOTES</span></span>

## <span data-ttu-id="99307-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99307-141">RELATED LINKS</span></span>

[<span data-ttu-id="99307-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="99307-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="99307-143">Új – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="99307-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="99307-144">Új – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="99307-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="99307-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="99307-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


