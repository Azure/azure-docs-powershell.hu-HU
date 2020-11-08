---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016064"
---
# <span data-ttu-id="1eac3-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1eac3-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="1eac3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1eac3-102">SYNOPSIS</span></span>
<span data-ttu-id="1eac3-103">Módosítja a bevezetések állapotát, konfigurációs beállításait vagy frissítési módját.</span><span class="sxs-lookup"><span data-stu-id="1eac3-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="1eac3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1eac3-104">SYNTAX</span></span>

### <span data-ttu-id="1eac3-105">Frissítés</span><span class="sxs-lookup"><span data-stu-id="1eac3-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1eac3-106">Config</span><span class="sxs-lookup"><span data-stu-id="1eac3-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1eac3-107">Állapot</span><span class="sxs-lookup"><span data-stu-id="1eac3-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1eac3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1eac3-108">DESCRIPTION</span></span>
<span data-ttu-id="1eac3-109">A **set-AzureDeployment** parancsmag az Azure-példányok állapotát, konfigurációs beállításait vagy frissítési módját módosítja.</span><span class="sxs-lookup"><span data-stu-id="1eac3-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="1eac3-110">A telepített példány állapotát a futás vagy a felfüggesztett állapotra is módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="1eac3-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="1eac3-111">Az. cscfg fájlt módosíthatja a központi telepítőben.</span><span class="sxs-lookup"><span data-stu-id="1eac3-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="1eac3-112">Beállíthatja a frissítési módot, és frissítheti a konfigurációs fájlokat.</span><span class="sxs-lookup"><span data-stu-id="1eac3-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="1eac3-113">A **set-AzureWalkUpgradeDomain** parancsmaggal frissítést kezdeményezhet.</span><span class="sxs-lookup"><span data-stu-id="1eac3-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="1eac3-114">Példák</span><span class="sxs-lookup"><span data-stu-id="1eac3-114">EXAMPLES</span></span>

### <span data-ttu-id="1eac3-115">Példa 1: a bevezetési állapot módosítása</span><span class="sxs-lookup"><span data-stu-id="1eac3-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="1eac3-116">Ez a parancs a ContosoService nevű szolgáltatás üzembe helyezésének állapotát a termelés környezetében állítja be.</span><span class="sxs-lookup"><span data-stu-id="1eac3-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="1eac3-117">2. példa: másik konfigurációs fájl hozzárendelése egy központi példányhoz</span><span class="sxs-lookup"><span data-stu-id="1eac3-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="1eac3-118">Ez a parancs egy másik konfigurációs fájlt rendel a ContosoService nevű szolgáltatás üzembe helyezéséhez a megállóhelyek környezetében.</span><span class="sxs-lookup"><span data-stu-id="1eac3-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="1eac3-119">3. példa: a frissítési mód beállítása automatikusra</span><span class="sxs-lookup"><span data-stu-id="1eac3-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="1eac3-120">Ezzel a paranccsal automatikusan beállíthatja a frissítési módot, és megad egy frissítési csomagot és egy új konfigurációs fájlt.</span><span class="sxs-lookup"><span data-stu-id="1eac3-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="1eac3-121">4. példa: a bővítmények konfigurációjának telepítése egy szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="1eac3-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="1eac3-122">Ez a parancs a megadott Felhőbeli szolgáltatásban telepíti a bővítmények konfigurációját, és alkalmazza őket a szerepkörökre.</span><span class="sxs-lookup"><span data-stu-id="1eac3-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="1eac3-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1eac3-123">PARAMETERS</span></span>

### <span data-ttu-id="1eac3-124">-Config</span><span class="sxs-lookup"><span data-stu-id="1eac3-124">-Config</span></span>
<span data-ttu-id="1eac3-125">Azt adja meg, hogy a parancsmag módosítja-e a telepített példány konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1eac3-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-126">-Configuration</span><span class="sxs-lookup"><span data-stu-id="1eac3-126">-Configuration</span></span>
<span data-ttu-id="1eac3-127">A. cscfg konfigurációs fájlok teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="1eac3-128">Megadhat egy konfigurációs fájlt a frissítéshez vagy a konfiguráció módosításához.</span><span class="sxs-lookup"><span data-stu-id="1eac3-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="1eac3-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="1eac3-130">A bővítmények konfigurációs objektumainak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-131">-Force</span><span class="sxs-lookup"><span data-stu-id="1eac3-131">-Force</span></span>
<span data-ttu-id="1eac3-132">Azt jelzi, hogy a parancsmag kényszerített frissítést hajt végre.</span><span class="sxs-lookup"><span data-stu-id="1eac3-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1eac3-133">-InformationAction</span></span>
<span data-ttu-id="1eac3-134">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="1eac3-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1eac3-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1eac3-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1eac3-136">Folytassa</span><span class="sxs-lookup"><span data-stu-id="1eac3-136">Continue</span></span>
- <span data-ttu-id="1eac3-137">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="1eac3-137">Ignore</span></span>
- <span data-ttu-id="1eac3-138">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="1eac3-138">Inquire</span></span>
- <span data-ttu-id="1eac3-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1eac3-139">SilentlyContinue</span></span>
- <span data-ttu-id="1eac3-140">állj</span><span class="sxs-lookup"><span data-stu-id="1eac3-140">Stop</span></span>
- <span data-ttu-id="1eac3-141">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="1eac3-141">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1eac3-142">-InformationVariable</span></span>
<span data-ttu-id="1eac3-143">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-143">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-144">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="1eac3-144">-Label</span></span>
<span data-ttu-id="1eac3-145">A frissített példány feliratát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-146">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="1eac3-146">-Mode</span></span>
<span data-ttu-id="1eac3-147">A frissítés üzemmódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="1eac3-148">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="1eac3-148">Valid values are:</span></span> 

- <span data-ttu-id="1eac3-149">Automatikus</span><span class="sxs-lookup"><span data-stu-id="1eac3-149">Auto</span></span> 
- <span data-ttu-id="1eac3-150">Kézi</span><span class="sxs-lookup"><span data-stu-id="1eac3-150">Manual</span></span> 
- <span data-ttu-id="1eac3-151">Egyidejű</span><span class="sxs-lookup"><span data-stu-id="1eac3-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="1eac3-152">-NewStatus</span></span>
<span data-ttu-id="1eac3-153">A bevezetéshez tartozó cél állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="1eac3-154">Az érvényes értékek a következők: futás és felfüggesztve.</span><span class="sxs-lookup"><span data-stu-id="1eac3-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-155">-Package (csomag)</span><span class="sxs-lookup"><span data-stu-id="1eac3-155">-Package</span></span>
<span data-ttu-id="1eac3-156">A frissítési csomagfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-157">-Profil</span><span class="sxs-lookup"><span data-stu-id="1eac3-157">-Profile</span></span>
<span data-ttu-id="1eac3-158">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1eac3-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1eac3-159">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1eac3-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="1eac3-160">-RoleName</span></span>
<span data-ttu-id="1eac3-161">A frissítendő szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-162">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="1eac3-162">-ServiceName</span></span>
<span data-ttu-id="1eac3-163">A központi üzembe helyezés Azure-szolgáltatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-163">Specifies the name of the Azure service of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-164">-Slot</span><span class="sxs-lookup"><span data-stu-id="1eac3-164">-Slot</span></span>
<span data-ttu-id="1eac3-165">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1eac3-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="1eac3-166">Érvényes értékek: a termelés és a megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="1eac3-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-167">-Állapot</span><span class="sxs-lookup"><span data-stu-id="1eac3-167">-Status</span></span>
<span data-ttu-id="1eac3-168">Azt adja meg, hogy a parancsmag a telepített példány állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="1eac3-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-169">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="1eac3-169">-Upgrade</span></span>
<span data-ttu-id="1eac3-170">Azt adja meg, hogy az adott parancsmag frissíti a telepítőt.</span><span class="sxs-lookup"><span data-stu-id="1eac3-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eac3-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eac3-171">CommonParameters</span></span>
<span data-ttu-id="1eac3-172">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1eac3-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eac3-173">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eac3-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eac3-174">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1eac3-174">INPUTS</span></span>

## <span data-ttu-id="1eac3-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1eac3-175">OUTPUTS</span></span>

## <span data-ttu-id="1eac3-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1eac3-176">NOTES</span></span>

## <span data-ttu-id="1eac3-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1eac3-177">RELATED LINKS</span></span>

[<span data-ttu-id="1eac3-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1eac3-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="1eac3-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="1eac3-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="1eac3-180">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1eac3-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="1eac3-181">Új – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1eac3-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="1eac3-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1eac3-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="1eac3-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="1eac3-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


