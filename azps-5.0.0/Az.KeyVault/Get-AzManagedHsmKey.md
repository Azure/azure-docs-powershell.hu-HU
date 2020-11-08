---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185308"
---
# <span data-ttu-id="98fda-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98fda-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="98fda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98fda-102">SYNOPSIS</span></span>
<span data-ttu-id="98fda-103">Felügyelt HSM-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="98fda-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="98fda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98fda-104">SYNTAX</span></span>

### <span data-ttu-id="98fda-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98fda-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="98fda-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="98fda-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="98fda-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="98fda-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="98fda-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="98fda-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="98fda-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fda-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="98fda-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98fda-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="98fda-114">DESCRIPTION</span></span>
<span data-ttu-id="98fda-115">A **Get-AzManagedHsmKey** parancsmag Azure Managed HSM-kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="98fda-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="98fda-116">Ez a parancsmag a **Microsoft. Azure. commands.-Vault. models. debundle** vagy a felügyelt HSM vagy verziószámmal rendelkező összes **köteg** objektum listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="98fda-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="98fda-117">Példák</span><span class="sxs-lookup"><span data-stu-id="98fda-117">EXAMPLES</span></span>

### <span data-ttu-id="98fda-118">Példa 1: a felügyelt HSM összes kulcsának lekérése</span><span class="sxs-lookup"><span data-stu-id="98fda-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="98fda-119">Boltozat/HSM név: testmhsm név: testkey001 verzió: azonosító: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 enabled: true lejárat: not not this: created: 10/14/2020 3:39:16 frissítve: 10/14/2020 3:39:16 am helyreállítási szint: visszanyerhető + törölhető Címkék:</span><span class="sxs-lookup"><span data-stu-id="98fda-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="98fda-120">Boltozat/HSM név: testmhsm név: testkey002 verzió: azonosító: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 enabled: false lejár: 10/14/2022 8:13:29 nem vagyok a következő: 10/14/2020 8:13:33 am created: 10/14/2020 8:14:01 frissítve: 10/14/2020 8:14:01 am helyreállítási szint:</span><span class="sxs-lookup"><span data-stu-id="98fda-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="98fda-121">Ez a parancs a testmhsm nevű felügyelt HSM kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98fda-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="98fda-122">2. példa: a kulcs aktuális verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="98fda-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="98fda-123">Ez a parancs a testkey001 nevű kulcs aktuális verzióját kapja meg a testmhsm nevű felügyelt HSM-ben.</span><span class="sxs-lookup"><span data-stu-id="98fda-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="98fda-124">Megjegyzés: a HSM-név $hsm szerezhető be. VaultName</span><span class="sxs-lookup"><span data-stu-id="98fda-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="98fda-125">3. példa: a kulcsok minden verziójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="98fda-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="98fda-126">Ez a parancs a testkey001 nevű kulcsot a testmhsm nevű felügyelt HSM-ban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98fda-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="98fda-127">Példa 4: a kulcs meghatározott verziójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="98fda-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98fda-128">Ez a parancs a testkey nevű kulcs adott verzióját kapja meg a testmhsm nevű felügyelt HSM-ben.</span><span class="sxs-lookup"><span data-stu-id="98fda-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="98fda-129">Miután futtatta ezt a parancsot, a $Key objektumban való navigálással ellenőrizheti a billentyűk különböző tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="98fda-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="98fda-130">Példa 5: a felügyelt HSM-hez törölt, de el nem távolított billentyűk beolvasása</span><span class="sxs-lookup"><span data-stu-id="98fda-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="98fda-131">Ez a parancs a testmhsm nevű felügyelt HSM által korábban törölt, de el nem távolított billentyűket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98fda-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="98fda-132">6. példa: a felügyelt HSM-hez törölt, de nem véglegesen törölt kulcs testkey kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98fda-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="98fda-133">Ez a parancs a testmhsm nevű felügyelt HSM által korábban törölt, de nem véglegesen törölt kulcs testkey kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98fda-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="98fda-134">Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt kulcs ütemezett leöblítési dátumát.</span><span class="sxs-lookup"><span data-stu-id="98fda-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="98fda-135">7. példa: a felügyelt HSM összes kulcsának beolvasása szűréssel</span><span class="sxs-lookup"><span data-stu-id="98fda-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98fda-136">Ez a parancs a "teszt" kezdetű testmhsm nevű felügyelt HSM kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98fda-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="98fda-137">8. példa: nyilvános kulcs letöltése. PEM fájlként</span><span class="sxs-lookup"><span data-stu-id="98fda-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98fda-138">Az RSA-kulcsok nyilvános kulcsát a paraméter megadásával töltheti le `-OutFile` .</span><span class="sxs-lookup"><span data-stu-id="98fda-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="98fda-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98fda-139">PARAMETERS</span></span>

### <span data-ttu-id="98fda-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fda-140">-DefaultProfile</span></span>
<span data-ttu-id="98fda-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98fda-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98fda-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="98fda-142">-HsmName</span></span>
<span data-ttu-id="98fda-143">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="98fda-143">HSM name.</span></span> <span data-ttu-id="98fda-144">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="98fda-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="98fda-145">-IncludeVersions</span></span>
<span data-ttu-id="98fda-146">Meghatározza, hogy a kulcs verziószámait szeretné-e szerepeltetni a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="98fda-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98fda-147">-InputObject</span></span>
<span data-ttu-id="98fda-148">HSM-objektum.</span><span class="sxs-lookup"><span data-stu-id="98fda-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="98fda-149">-InRemovedState</span></span>
<span data-ttu-id="98fda-150">Itt adhatja meg, hogy megjelenjen-e a korábban törölt kulcsok a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="98fda-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-151">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98fda-151">-Name</span></span>
<span data-ttu-id="98fda-152">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="98fda-152">Key name.</span></span>
<span data-ttu-id="98fda-153">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet és a kulcsnév alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="98fda-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-154">-Fájl kilépése</span><span class="sxs-lookup"><span data-stu-id="98fda-154">-OutFile</span></span>
<span data-ttu-id="98fda-155">Azt a kimeneti fájlt adja meg, amelyre a parancsmag menti a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="98fda-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="98fda-156">A nyilvános kulcs alapértelmezés szerint PEM formátumban lett mentve.</span><span class="sxs-lookup"><span data-stu-id="98fda-156">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98fda-157">-ResourceId</span></span>
<span data-ttu-id="98fda-158">HSM-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="98fda-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-159">-Verzió</span><span class="sxs-lookup"><span data-stu-id="98fda-159">-Version</span></span>
<span data-ttu-id="98fda-160">Fő verzió.</span><span class="sxs-lookup"><span data-stu-id="98fda-160">Key version.</span></span>
<span data-ttu-id="98fda-161">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet, a kulcs neve és a kulcs verziója alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="98fda-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fda-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fda-162">CommonParameters</span></span>
<span data-ttu-id="98fda-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98fda-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fda-164">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="98fda-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fda-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98fda-165">INPUTS</span></span>

### <span data-ttu-id="98fda-166">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="98fda-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98fda-167">System. String</span><span class="sxs-lookup"><span data-stu-id="98fda-167">System.String</span></span>

## <span data-ttu-id="98fda-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98fda-168">OUTPUTS</span></span>

### <span data-ttu-id="98fda-169">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="98fda-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98fda-170">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="98fda-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="98fda-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98fda-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98fda-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98fda-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="98fda-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98fda-173">NOTES</span></span>

## <span data-ttu-id="98fda-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98fda-174">RELATED LINKS</span></span>

[<span data-ttu-id="98fda-175">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98fda-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="98fda-176">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98fda-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="98fda-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98fda-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="98fda-178">Visszavonás – AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="98fda-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="98fda-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98fda-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="98fda-180">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98fda-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)