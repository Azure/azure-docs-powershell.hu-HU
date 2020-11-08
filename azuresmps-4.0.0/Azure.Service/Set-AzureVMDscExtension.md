---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017351"
---
# <span data-ttu-id="3448a-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="3448a-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="3448a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3448a-102">SYNOPSIS</span></span>
<span data-ttu-id="3448a-103">A DSC bővítmény beállítása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="3448a-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="3448a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3448a-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3448a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3448a-105">DESCRIPTION</span></span>
<span data-ttu-id="3448a-106">A **set-AzureVMDscExtension** parancsmag a kívánt állapot-konfiguráció (DSC) kiterjesztését egy virtuális gépen állítja be.</span><span class="sxs-lookup"><span data-stu-id="3448a-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="3448a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3448a-107">EXAMPLES</span></span>

### <span data-ttu-id="3448a-108">1. példa: a DSC-bővítmény beállítása virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="3448a-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="3448a-109">Ez a parancs a DSC bővítményt egy virtuális gépen állítja be.</span><span class="sxs-lookup"><span data-stu-id="3448a-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="3448a-110">A MyConfiguration.ps1.zip csomagot előzőleg az Azure-tárhelyre kell feltölteni a **Közzététel – AzureVMDscConfiguration** parancs segítségével, és az MyConfiguration.ps1 parancsfájlt és az attól függ, hogy milyen modulokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3448a-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="3448a-111">A MyConfiguration argumentum az adott DSC-konfigurációt jelzi a végrehajtandó parancsfájlon belül.</span><span class="sxs-lookup"><span data-stu-id="3448a-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="3448a-112">A- *ConfigurationArgument* paraméter a konfigurációs függvénynek átadott argumentumokat tartalmazó Hashtable ad meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="3448a-113">2. példa: a DSC-bővítmény konfigurálása virtuális gépen a konfigurációs adatokat tartalmazó útvonal használatával</span><span class="sxs-lookup"><span data-stu-id="3448a-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="3448a-114">Ez a parancs a DSC bővítményt egy virtuális gépen a konfigurációs adatelérési út segítségével állítja be.</span><span class="sxs-lookup"><span data-stu-id="3448a-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="3448a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3448a-115">PARAMETERS</span></span>

### <span data-ttu-id="3448a-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="3448a-116">-ConfigurationArchive</span></span>
<span data-ttu-id="3448a-117">Annak a konfigurációs csomagnak (. zip fájlnak) a nevét adja meg, amelyet korábban a közzététel – AzureVMDscConfiguration feltöltött.</span><span class="sxs-lookup"><span data-stu-id="3448a-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="3448a-118">Ehhez a paraméterhez csak a fájl nevét kell megadni elérési út nélkül.</span><span class="sxs-lookup"><span data-stu-id="3448a-118">This parameter must specify only the name of the file, without any path.</span></span>

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

### <span data-ttu-id="3448a-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="3448a-119">-ConfigurationArgument</span></span>
<span data-ttu-id="3448a-120">A konfigurációs függvény argumentumait megadó Hashtable adja meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="3448a-121">A kulcsok megfelelnek a paraméterek neveinek és a paraméter értékeinek.</span><span class="sxs-lookup"><span data-stu-id="3448a-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="3448a-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3448a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3448a-123">primitív típusok</span><span class="sxs-lookup"><span data-stu-id="3448a-123">primitive types</span></span>
- <span data-ttu-id="3448a-124">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="3448a-124">string</span></span>
- <span data-ttu-id="3448a-125">tömb</span><span class="sxs-lookup"><span data-stu-id="3448a-125">array</span></span>
- <span data-ttu-id="3448a-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="3448a-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="3448a-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="3448a-128">Annak a. psd1 fájlnak az elérési útját adja meg, amely a konfigurációs függvény adatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="3448a-129">Ennek a fájlnak a konfigurációs és környezeti adatainak elkülönítése című témakörben leírtak szerint tartalmaznia kell egy Hashtable https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="3448a-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3448a-130">-ConfigurationName</span></span>
<span data-ttu-id="3448a-131">A DSC bővítmény által kezdeményezett konfigurációs parancsfájl vagy modul nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="3448a-132">Ennek a paraméternek az értékének a *ConfigurationArchive* -ban csomagolt parancsfájlokban vagy modulokban található egyik konfigurációs függvény nevének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3448a-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="3448a-133">Ez a parancsmag alapértelmezés szerint a *ConfigurationArchive* paraméter által megadott fájl nevét adja meg, ha ezt a paramétert kihagyja a kiterjesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="3448a-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="3448a-134">Ha például a *ConfigurationArchive* "SalesWebSite.ps1.zip", a *ConfigurationName* alapértelmezett értéke "SalesWebSite".</span><span class="sxs-lookup"><span data-stu-id="3448a-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-135">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3448a-135">-ContainerName</span></span>
<span data-ttu-id="3448a-136">Annak az Azure-tárolónak a nevét adja meg, ahol a *ConfigurationArchive* található.</span><span class="sxs-lookup"><span data-stu-id="3448a-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="3448a-137">-DataCollection</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-138">-Force</span><span class="sxs-lookup"><span data-stu-id="3448a-138">-Force</span></span>
<span data-ttu-id="3448a-139">Jelzi, hogy ez a parancsmag felülírja a meglévő Blobs-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="3448a-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

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

### <span data-ttu-id="3448a-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3448a-140">-InformationAction</span></span>
<span data-ttu-id="3448a-141">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3448a-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3448a-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3448a-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3448a-143">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3448a-143">Continue</span></span>
- <span data-ttu-id="3448a-144">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3448a-144">Ignore</span></span>
- <span data-ttu-id="3448a-145">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3448a-145">Inquire</span></span>
- <span data-ttu-id="3448a-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3448a-146">SilentlyContinue</span></span>
- <span data-ttu-id="3448a-147">állj</span><span class="sxs-lookup"><span data-stu-id="3448a-147">Stop</span></span>
- <span data-ttu-id="3448a-148">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3448a-148">Suspend</span></span>

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

### <span data-ttu-id="3448a-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3448a-149">-InformationVariable</span></span>
<span data-ttu-id="3448a-150">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3448a-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="3448a-151">-Profile</span></span>
<span data-ttu-id="3448a-152">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3448a-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3448a-153">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3448a-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3448a-154">-Hivatkozásnév</span><span class="sxs-lookup"><span data-stu-id="3448a-154">-ReferenceName</span></span>
<span data-ttu-id="3448a-155">Olyan felhasználó által definiált karakterláncot ad meg, amely a kiterjesztésre hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="3448a-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="3448a-156">Ezt a paramétert akkor adja meg a program, ha a bővítményt első alkalommal felveszi a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="3448a-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="3448a-157">A későbbi frissítésekhez a bővítmény frissítésekor meg kell adnia a korábban használt hivatkozási nevet.</span><span class="sxs-lookup"><span data-stu-id="3448a-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="3448a-158">A bővítményhez rendelt *hivatkozásnév* a **Get-AzureVM** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="3448a-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="3448a-159">-StorageContext</span></span>
<span data-ttu-id="3448a-160">Itt adhatja meg a konfigurációs parancsfájl eléréséhez használt biztonsági beállításokat tartalmazó Azure Storage Context-környezetet.</span><span class="sxs-lookup"><span data-stu-id="3448a-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="3448a-161">Ez a környezet olvasási hozzáférést biztosít a *ContainerName* paraméter által megadott tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="3448a-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3448a-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="3448a-163">Az összes tárolási szolgáltatás (például "core.contoso.net") DNS-végpontjának utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-164">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3448a-164">-Version</span></span>
<span data-ttu-id="3448a-165">A DSC bővítmény adott verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="3448a-166">Ha ez a paraméter nincs megadva, az alapértelmezett érték az "1. \*" értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="3448a-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-167">-VM</span><span class="sxs-lookup"><span data-stu-id="3448a-167">-VM</span></span>
<span data-ttu-id="3448a-168">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3448a-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="3448a-169">-WmfVersion</span></span>
<span data-ttu-id="3448a-170">A Windows Management Framework (WMF) verziószámát adja meg a virtuális gépre való telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="3448a-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="3448a-171">A DSC bővítmény az olyan DSC-funkcióktól függ, amelyek csak a WMF frissítéseiben érhetők el.</span><span class="sxs-lookup"><span data-stu-id="3448a-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="3448a-172">Ez a paraméter adja meg, hogy a frissítés melyik verziójára telepítse a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="3448a-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="3448a-173">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3448a-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3448a-174">4,0-ban.</span><span class="sxs-lookup"><span data-stu-id="3448a-174">4.0.</span></span>
<span data-ttu-id="3448a-175">A WMF 4,0 telepítése csak akkor, ha már telepítve van egy újabb verzió.</span><span class="sxs-lookup"><span data-stu-id="3448a-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="3448a-176">5,0-ban.</span><span class="sxs-lookup"><span data-stu-id="3448a-176">5.0.</span></span>
<span data-ttu-id="3448a-177">A WMF 5,0 legújabb verziójának telepítése.</span><span class="sxs-lookup"><span data-stu-id="3448a-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="3448a-178">legújabb.</span><span class="sxs-lookup"><span data-stu-id="3448a-178">latest.</span></span>
<span data-ttu-id="3448a-179">A legújabb WMF, jelenleg WMF 5,0 telepítése.</span><span class="sxs-lookup"><span data-stu-id="3448a-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="3448a-180">Az alapértelmezett érték a legújabb.</span><span class="sxs-lookup"><span data-stu-id="3448a-180">The default value is latest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3448a-181">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3448a-181">-Confirm</span></span>
<span data-ttu-id="3448a-182">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3448a-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3448a-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3448a-183">-WhatIf</span></span>
<span data-ttu-id="3448a-184">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3448a-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3448a-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3448a-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3448a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3448a-186">CommonParameters</span></span>
<span data-ttu-id="3448a-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3448a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3448a-188">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3448a-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3448a-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3448a-189">INPUTS</span></span>

## <span data-ttu-id="3448a-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3448a-190">OUTPUTS</span></span>

## <span data-ttu-id="3448a-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3448a-191">NOTES</span></span>

## <span data-ttu-id="3448a-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3448a-192">RELATED LINKS</span></span>

[<span data-ttu-id="3448a-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="3448a-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="3448a-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="3448a-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="3448a-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="3448a-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="3448a-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3448a-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="3448a-197">Közzététel – AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3448a-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


