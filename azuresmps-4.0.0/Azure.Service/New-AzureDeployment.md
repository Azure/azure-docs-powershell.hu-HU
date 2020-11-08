---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015929"
---
# <span data-ttu-id="b1ffb-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b1ffb-101">New-AzureDeployment</span></span>

## <span data-ttu-id="b1ffb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ffb-103">Egy szolgáltatásból hozza létre a telepítőt.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="b1ffb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1ffb-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1ffb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="b1ffb-106">A **New-AzureDeployment** parancsmag egy olyan szolgáltatásból hoz létre Azure-telepítőt, amely a webes szerepköröket és a munkatársi szerepköröket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="b1ffb-107">Ez a parancsmag egy csomagfájl (. cspkg) és egy szolgáltatás-konfigurációs fájl (. cscfg) alapján hoz létre központi üzembe helyezést.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="b1ffb-108">Adjon meg egy olyan nevet, amely egyedi a központi telepítő környezeten belül.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="b1ffb-109">A **New-AzureVM** parancsmaggal az Azure virtuális gépeken alapuló központi telepítőt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="b1ffb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b1ffb-110">EXAMPLES</span></span>

### <span data-ttu-id="b1ffb-111">Példa 1: központi telepítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="b1ffb-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="b1ffb-112">A parancs a ContosoPackage. cspkg nevű csomagon alapuló, a ContosoConfiguration. cscfg nevű konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="b1ffb-113">A parancs a központi telepítő címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="b1ffb-114">Nem adja meg a nevet.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-114">It does not specify a name.</span></span>
<span data-ttu-id="b1ffb-115">Ez a parancsmag létrehoz egy GUID-azonosítót névként.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="b1ffb-116">2. példa: a központi telepítő létrehozása bővítmény-konfiguráció alapján</span><span class="sxs-lookup"><span data-stu-id="b1ffb-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="b1ffb-117">Ezzel a paranccsal létrehozhatja a termelést a csomag és a konfiguráció alapján.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="b1ffb-118">A parancs a ContosoExtensionConfig. cscfg nevű bővítmény-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="b1ffb-119">Ez a parancsmag a nevet és a címkét AZONOSÍTÓkat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="b1ffb-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1ffb-120">PARAMETERS</span></span>

### <span data-ttu-id="b1ffb-121">-Configuration</span><span class="sxs-lookup"><span data-stu-id="b1ffb-121">-Configuration</span></span>
<span data-ttu-id="b1ffb-122">A szolgáltatás konfigurációs fájljának teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ffb-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="b1ffb-123">-DoNotStart</span></span>
<span data-ttu-id="b1ffb-124">Azt adja meg, hogy ez a parancsmag nem indítja el a telepített példányt.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-124">Specifies that this cmdlet does not start the deployment.</span></span>

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

### <span data-ttu-id="b1ffb-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1ffb-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="b1ffb-126">A bővítmények konfigurációs objektumainak tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ffb-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b1ffb-127">-InformationAction</span></span>
<span data-ttu-id="b1ffb-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b1ffb-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b1ffb-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1ffb-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b1ffb-130">Continue</span></span>
- <span data-ttu-id="b1ffb-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b1ffb-131">Ignore</span></span>
- <span data-ttu-id="b1ffb-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b1ffb-132">Inquire</span></span>
- <span data-ttu-id="b1ffb-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b1ffb-133">SilentlyContinue</span></span>
- <span data-ttu-id="b1ffb-134">állj</span><span class="sxs-lookup"><span data-stu-id="b1ffb-134">Stop</span></span>
- <span data-ttu-id="b1ffb-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b1ffb-135">Suspend</span></span>

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

### <span data-ttu-id="b1ffb-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b1ffb-136">-InformationVariable</span></span>
<span data-ttu-id="b1ffb-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b1ffb-138">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="b1ffb-138">-Label</span></span>
<span data-ttu-id="b1ffb-139">A bevezetéshez a címke nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="b1ffb-140">Ha nem ad meg címkét, ez a parancsmag GUID-ot használ.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ffb-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1ffb-141">-Name</span></span>
<span data-ttu-id="b1ffb-142">A telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-142">Specifies a deployment name.</span></span>
<span data-ttu-id="b1ffb-143">Ha nem ad meg nevet, ez a parancsmag GUID-ot használ.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ffb-144">-Package (csomag)</span><span class="sxs-lookup"><span data-stu-id="b1ffb-144">-Package</span></span>
<span data-ttu-id="b1ffb-145">Egy. cspkg fájl elérési útját vagy URI-azonosítóját adja meg ugyanazon az előfizetésen vagy projekten belül.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1ffb-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1ffb-146">-Profile</span></span>
<span data-ttu-id="b1ffb-147">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1ffb-148">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1ffb-149">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="b1ffb-149">-ServiceName</span></span>
<span data-ttu-id="b1ffb-150">A központi üzembe helyezés Azure-szolgáltatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-150">Specifies the name of the Azure service for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ffb-151">-Slot</span><span class="sxs-lookup"><span data-stu-id="b1ffb-151">-Slot</span></span>
<span data-ttu-id="b1ffb-152">Azt a környezetet adja meg, ahol ez a parancsmag hozza létre a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="b1ffb-153">Érvényes értékek: staging és termelés.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="b1ffb-154">Az alapértelmezett érték a termelés.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1ffb-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="b1ffb-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="b1ffb-156">Itt adhatja meg, hogy a figyelmeztető üzenetek hibásak-e.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="b1ffb-157">Ha ezt a paramétert adja meg, figyelmeztető üzenet jelzi, hogy a telepítő sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="b1ffb-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

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

### <span data-ttu-id="b1ffb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ffb-158">CommonParameters</span></span>
<span data-ttu-id="b1ffb-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1ffb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ffb-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1ffb-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ffb-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1ffb-161">INPUTS</span></span>

## <span data-ttu-id="b1ffb-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1ffb-162">OUTPUTS</span></span>

## <span data-ttu-id="b1ffb-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1ffb-163">NOTES</span></span>

## <span data-ttu-id="b1ffb-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1ffb-164">RELATED LINKS</span></span>

[<span data-ttu-id="b1ffb-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b1ffb-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="b1ffb-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="b1ffb-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="b1ffb-167">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b1ffb-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="b1ffb-168">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="b1ffb-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="b1ffb-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b1ffb-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="b1ffb-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b1ffb-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


