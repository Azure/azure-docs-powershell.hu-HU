---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015883"
---
# <span data-ttu-id="e3893-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="e3893-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="e3893-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3893-102">SYNOPSIS</span></span>
<span data-ttu-id="e3893-103">Az aktuális szolgáltatás közzététele a Windows Azure-ban</span><span class="sxs-lookup"><span data-stu-id="e3893-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="e3893-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3893-104">SYNTAX</span></span>

### <span data-ttu-id="e3893-105">PublishFromServiceDefinition (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3893-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e3893-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="e3893-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3893-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3893-107">DESCRIPTION</span></span>
<span data-ttu-id="e3893-108">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="e3893-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e3893-109">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e3893-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e3893-110">A **Közzététel – AzureServiceProject** parancsmag közzéteszi az aktuális szolgáltatást a felhőben.</span><span class="sxs-lookup"><span data-stu-id="e3893-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="e3893-111">Megadhatja a közzétételi konfigurációt (például az **előfizetést** , a **StorageAccountName** , a **helyet** , a **bővítőhelyet** ) a parancssorban vagy a **set-AzureServiceProject** parancsmagon keresztül.</span><span class="sxs-lookup"><span data-stu-id="e3893-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="e3893-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e3893-112">EXAMPLES</span></span>

### <span data-ttu-id="e3893-113">Példa 1: szolgáltatási projekt közzététele alapértelmezett értékekkel</span><span class="sxs-lookup"><span data-stu-id="e3893-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="e3893-114">Ez a példa közzéteszi az aktuális szolgáltatást a jelenlegi szolgáltatás beállításaival és az Azure aktuális közzétételi profiljának használatával.</span><span class="sxs-lookup"><span data-stu-id="e3893-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="e3893-115">2. példa: központi telepítőcsomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="e3893-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="e3893-116">Ez a példa létrehoz egy telepítőcsomag (. cspkg) fájlt a címtárszolgáltatásban, és nem teszi közzé a Windows Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e3893-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="e3893-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3893-117">PARAMETERS</span></span>

### <span data-ttu-id="e3893-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="e3893-118">-AffinityGroup</span></span>
<span data-ttu-id="e3893-119">Azt a affinitási csoportot adja meg, amelyet használni szeretne a szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e3893-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="e3893-120">-Configuration</span></span>
<span data-ttu-id="e3893-121">A szolgáltatás konfigurációs fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3893-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="e3893-122">Ha ezt a paramétert adja meg, adja meg a *csomag* paramétert.</span><span class="sxs-lookup"><span data-stu-id="e3893-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-123">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="e3893-123">-DeploymentName</span></span>
<span data-ttu-id="e3893-124">A központi telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3893-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="e3893-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-126">-Launch (indítás)</span><span class="sxs-lookup"><span data-stu-id="e3893-126">-Launch</span></span>
<span data-ttu-id="e3893-127">Megnyit egy böngészőablakot, amelyen megtekintheti az alkalmazást a telepítés után.</span><span class="sxs-lookup"><span data-stu-id="e3893-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="e3893-128">-Location</span></span>
<span data-ttu-id="e3893-129">Az a terület, ahol az alkalmazást üzemeltetni fogja.</span><span class="sxs-lookup"><span data-stu-id="e3893-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="e3893-130">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="e3893-130">Possible values are:</span></span> 
  
- <span data-ttu-id="e3893-131">Bárhonnan Ázsia</span><span class="sxs-lookup"><span data-stu-id="e3893-131">Anywhere Asia</span></span>
- <span data-ttu-id="e3893-132">Bárhol Európában</span><span class="sxs-lookup"><span data-stu-id="e3893-132">Anywhere Europe</span></span>
- <span data-ttu-id="e3893-133">Bárhol vagyunk</span><span class="sxs-lookup"><span data-stu-id="e3893-133">Anywhere US</span></span>
- <span data-ttu-id="e3893-134">Kelet-ázsiai</span><span class="sxs-lookup"><span data-stu-id="e3893-134">East Asia</span></span>
- <span data-ttu-id="e3893-135">Kelet-amerikai</span><span class="sxs-lookup"><span data-stu-id="e3893-135">East US</span></span>
- <span data-ttu-id="e3893-136">Közép-amerikai Észak-amerikai</span><span class="sxs-lookup"><span data-stu-id="e3893-136">North Central US</span></span>
- <span data-ttu-id="e3893-137">Észak-Európa</span><span class="sxs-lookup"><span data-stu-id="e3893-137">North Europe</span></span>
- <span data-ttu-id="e3893-138">Dél-Közép-amerikai</span><span class="sxs-lookup"><span data-stu-id="e3893-138">South Central US</span></span>
- <span data-ttu-id="e3893-139">Dél-ázsiai</span><span class="sxs-lookup"><span data-stu-id="e3893-139">Southeast Asia</span></span>
- <span data-ttu-id="e3893-140">Nyugat-Európa</span><span class="sxs-lookup"><span data-stu-id="e3893-140">West Europe</span></span>
- <span data-ttu-id="e3893-141">Nyugat-amerikai</span><span class="sxs-lookup"><span data-stu-id="e3893-141">West US</span></span>
 
<span data-ttu-id="e3893-142">Ha nincs megadva hely, a program az utolsó híváshoz megadott helyet fogja használni a **AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="e3893-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="e3893-143">Ha még nincs megadva tartózkodási hely, a hely véletlenszerűen lesz kiválasztva az "Észak-Közép-amerikai" és "Dél-Közép-amerikai" helyről.</span><span class="sxs-lookup"><span data-stu-id="e3893-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-144">-Package (csomag)</span><span class="sxs-lookup"><span data-stu-id="e3893-144">-Package</span></span>
<span data-ttu-id="e3893-145">A telepítendő csomagfájl meghatározása.</span><span class="sxs-lookup"><span data-stu-id="e3893-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="e3893-146">Adjon meg egy olyan helyi fájlt, amely. cspkg fájlnévkiterjesztéssel vagy a csomagot tartalmazó blob-AZONOSÍTÓval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e3893-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="e3893-147">Ha ezt a paramétert adja meg, ne adja meg a *szolgáltatásnév* paramétert.</span><span class="sxs-lookup"><span data-stu-id="e3893-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="e3893-148">-Profile</span></span>
<span data-ttu-id="e3893-149">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e3893-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3893-150">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e3893-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3893-151">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="e3893-151">-ServiceName</span></span>
<span data-ttu-id="e3893-152">Itt adhatja meg a Windows Azure-ra való közzétételkor a szolgáltatáshoz használni kívánt nevet.</span><span class="sxs-lookup"><span data-stu-id="e3893-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="e3893-153">A név határozza meg a címke azon részét a cloudapp.net altartományban, amellyel a szolgáltatás a Windows Azure-ban (azaz **név**. cloudapp.net) van tárolva.</span><span class="sxs-lookup"><span data-stu-id="e3893-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="e3893-154">A szolgáltatás közzétételekor megadott nevek felülírják a szolgáltatás létrehozásakor megadott nevet.</span><span class="sxs-lookup"><span data-stu-id="e3893-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="e3893-155">(Lásd a **New-AzureServiceProject** parancsmagot).</span><span class="sxs-lookup"><span data-stu-id="e3893-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-156">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3893-156">-Slot</span></span>
<span data-ttu-id="e3893-157">A szolgáltatáshoz használni kívánt telepítő-bővítőhely.</span><span class="sxs-lookup"><span data-stu-id="e3893-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="e3893-158">A lehetséges értékek "staging" és "termelés".</span><span class="sxs-lookup"><span data-stu-id="e3893-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="e3893-159">Ha nem ad meg bővítőhelyet, a rendszer az utolsó hívás Set-AzureDeploymentSlot-ban megadott bővítőhelyet használja.</span><span class="sxs-lookup"><span data-stu-id="e3893-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="e3893-160">Ha még nincs megadva bővítőhely, a program a "termelés" bővítőhelyet használja.</span><span class="sxs-lookup"><span data-stu-id="e3893-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3893-161">-StorageAccountName</span></span>
<span data-ttu-id="e3893-162">Annak a Windows Azure Storage-fióknak a nevét adja meg, amelyet a szolgáltatás közzétételekor kell használni.</span><span class="sxs-lookup"><span data-stu-id="e3893-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="e3893-163">Ezt az értéket csak a szolgáltatás közzétételéhez használja a program.</span><span class="sxs-lookup"><span data-stu-id="e3893-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="e3893-164">Ha ez a paraméter nincs megadva, a program az utolsó **set-AzureServiceProject** parancs értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e3893-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="e3893-165">Ha egyetlen tárterület sem volt megadva, a rendszer a szolgáltatás nevét tartalmazó tárterület-fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e3893-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="e3893-166">Ha nincs ilyen tárolási fiók, a parancsmag megkísérel létrehozni egy újat.</span><span class="sxs-lookup"><span data-stu-id="e3893-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="e3893-167">Ha azonban egy másik előfizetésben megtalálható a szolgáltatás nevéhez tartozó tárolási fiók, a kísérlet sikertelen lehet.</span><span class="sxs-lookup"><span data-stu-id="e3893-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3893-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3893-168">CommonParameters</span></span>
<span data-ttu-id="e3893-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3893-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3893-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3893-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3893-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3893-171">INPUTS</span></span>

## <span data-ttu-id="e3893-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3893-172">OUTPUTS</span></span>

## <span data-ttu-id="e3893-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3893-173">NOTES</span></span>

## <span data-ttu-id="e3893-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3893-174">RELATED LINKS</span></span>

[<span data-ttu-id="e3893-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="e3893-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="e3893-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="e3893-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


