---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195943"
---
# <span data-ttu-id="70d14-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="70d14-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="70d14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70d14-102">SYNOPSIS</span></span>
<span data-ttu-id="70d14-103">Egy felügyelt HSM kulcsát hozza létre, vagy egy kulcsot importál a felügyelt HSM-be.</span><span class="sxs-lookup"><span data-stu-id="70d14-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="70d14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70d14-104">SYNTAX</span></span>

### <span data-ttu-id="70d14-105">InteractiveCreate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70d14-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d14-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="70d14-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70d14-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="70d14-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d14-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="70d14-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70d14-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="70d14-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d14-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="70d14-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70d14-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="70d14-111">DESCRIPTION</span></span>
<span data-ttu-id="70d14-112">Az **Add-AzManagedHsmKey** parancsmag kulcsot hoz létre egy felügyelt HSM-ben az Azure Managed HSM-ben, vagy egy kulcsot importál a FELÜGYELt HSM-be.</span><span class="sxs-lookup"><span data-stu-id="70d14-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="70d14-113">Ezzel a parancsmaggal a következő módszerekkel adhat hozzá kulcsokat:</span><span class="sxs-lookup"><span data-stu-id="70d14-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="70d14-114">Alapértelmezett kulcs attribútumokat tartalmazó kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="70d14-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="70d14-115">Kulcs létrehozása az adott kulcs attribútumaival</span><span class="sxs-lookup"><span data-stu-id="70d14-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="70d14-116">Importáljon egy kulcsot egy. pfx fájlból a számítógépre.</span><span class="sxs-lookup"><span data-stu-id="70d14-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="70d14-117">A fenti műveletek bármelyikével alapvető attribútumokat adhat meg, illetve elfogadhat alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="70d14-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="70d14-118">Ha olyan kulcsot hoz létre vagy importál, amelynek a neve megegyezik a felügyelt HSM meglévő kulcsával, az eredeti kulcs frissül az új kulcshoz megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="70d14-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="70d14-119">A korábbi értékeket a kulcs adott verziójához tartozó, a verziószámot tartalmazó URI-azonosító használatával érheti el.</span><span class="sxs-lookup"><span data-stu-id="70d14-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="70d14-120">A főbb verziókkal és az URI-struktúrájával kapcsolatos tudnivalók a [kulcsok és a titkok](http://go.microsoft.com/fwlink/?linkid=518560) című témakörben olvashatók a felügyelt HSM REST API dokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="70d14-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="70d14-121">Példák</span><span class="sxs-lookup"><span data-stu-id="70d14-121">EXAMPLES</span></span>

### <span data-ttu-id="70d14-122">1. példa: RSA-HSM-kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="70d14-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="70d14-123">A parancs létrehoz egy testkey nevű RSA-HSM-kulcsot a testmhsm nevű felügyelt HSM testkey.</span><span class="sxs-lookup"><span data-stu-id="70d14-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="70d14-124">2. példa: EC-HSM-kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="70d14-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="70d14-125">Ez a parancs egy testkey nevű EC-HSM-kulcsot hoz létre, a testmhsm nevű felügyelt HSM testkey P-256 görbe használatával.</span><span class="sxs-lookup"><span data-stu-id="70d14-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="70d14-126">3. példa: TOT-HSM-kulcs létrehozása nem alapértelmezett értékekkel</span><span class="sxs-lookup"><span data-stu-id="70d14-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
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

<span data-ttu-id="70d14-127">Az első parancs a $KeyOperations változóban tárolja az értékeket dekódolja és ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="70d14-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="70d14-128">A második parancs létrehoz egy **datetime** típusú objektumot, amelyet az UTC a **Get-Date** parancsmag használatával definiál.</span><span class="sxs-lookup"><span data-stu-id="70d14-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="70d14-129">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="70d14-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="70d14-130">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="70d14-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="70d14-131">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="70d14-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="70d14-132">A harmadik parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="70d14-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="70d14-133">Az objektum a jelenlegi UTC időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d14-133">That object specifies current UTC time.</span></span> <span data-ttu-id="70d14-134">A parancs a $NotBefore változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="70d14-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="70d14-135">A végleges parancs létrehoz egy testkey nevű kulcsot, amely egy TOT-HSM kulcs.</span><span class="sxs-lookup"><span data-stu-id="70d14-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="70d14-136">A parancs a $KeyOperations tárolt, engedélyezett műveletek értékeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d14-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="70d14-137">A parancs az előző parancsokban létrehozott *lejáratok* és *NotBefore* paramétereinek időpontját adja meg, valamint a nagy SÚLYOSSÁGú és az IT-címkéket.</span><span class="sxs-lookup"><span data-stu-id="70d14-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="70d14-138">Az új kulcs le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="70d14-138">The new key is disabled.</span></span> <span data-ttu-id="70d14-139">Az **Update-AzManagedHsmKey** parancsmag használatával engedélyezheti azt.</span><span class="sxs-lookup"><span data-stu-id="70d14-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="70d14-140">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70d14-140">PARAMETERS</span></span>

### <span data-ttu-id="70d14-141">-CurveName</span><span class="sxs-lookup"><span data-stu-id="70d14-141">-CurveName</span></span>
<span data-ttu-id="70d14-142">Az elliptikus görbületű kriptográfia görbületi nevét adja meg, ez az érték akkor érvényes, ha a típus értéke EK.</span><span class="sxs-lookup"><span data-stu-id="70d14-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="70d14-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d14-143">-DefaultProfile</span></span>
<span data-ttu-id="70d14-144">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70d14-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70d14-145">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="70d14-145">-Disable</span></span>
<span data-ttu-id="70d14-146">Azt jelzi, hogy a felvenni kívánt kulcs a letiltott állapotú eredeti állapotra van állítva.</span><span class="sxs-lookup"><span data-stu-id="70d14-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="70d14-147">A billentyű használatát minden próbálkozás sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="70d14-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="70d14-148">Akkor használja ezt a paramétert, ha előre betöltődik a később engedélyezni kívánt billentyűk.</span><span class="sxs-lookup"><span data-stu-id="70d14-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="70d14-149">-Lejár</span><span class="sxs-lookup"><span data-stu-id="70d14-149">-Expires</span></span>
<span data-ttu-id="70d14-150">A kulcs lejárati időpontját adja meg az UTC-ben.</span><span class="sxs-lookup"><span data-stu-id="70d14-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="70d14-151">Ha nem adja meg, akkor a billentyű nem jár le.</span><span class="sxs-lookup"><span data-stu-id="70d14-151">If not specified, key will not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="70d14-152">-HsmName</span></span>
<span data-ttu-id="70d14-153">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="70d14-153">HSM name.</span></span> <span data-ttu-id="70d14-154">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="70d14-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70d14-155">-InputObject</span></span>
<span data-ttu-id="70d14-156">HSM-objektum.</span><span class="sxs-lookup"><span data-stu-id="70d14-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="70d14-157">-KeyFilePassword</span></span>
<span data-ttu-id="70d14-158">Az importálandó fontos anyagot tartalmazó helyi fájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="70d14-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-159">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="70d14-159">-KeyFilePath</span></span>
<span data-ttu-id="70d14-160">Az importálandó fő anyagot tartalmazó helyi fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="70d14-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="70d14-161">-KeyOps</span></span>
<span data-ttu-id="70d14-162">A kulccsal elvégezhető műveletek.</span><span class="sxs-lookup"><span data-stu-id="70d14-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="70d14-163">Ha nem látható, az összes művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="70d14-163">If not present, all operations can be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-164">-Típus</span><span class="sxs-lookup"><span data-stu-id="70d14-164">-KeyType</span></span>
<span data-ttu-id="70d14-165">A kulcs típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d14-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-166">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70d14-166">-Name</span></span>
<span data-ttu-id="70d14-167">Fontos név.</span><span class="sxs-lookup"><span data-stu-id="70d14-167">Key name.</span></span>
<span data-ttu-id="70d14-168">Parancsmag: a felügyelt HSM-név, az aktuálisan kijelölt környezet és a kulcsnév alapján egy kulcs teljes tartománynevét építi fel.</span><span class="sxs-lookup"><span data-stu-id="70d14-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="70d14-169">-NotBefore</span></span>
<span data-ttu-id="70d14-170">Az az UTC-idő, ameddig a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="70d14-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="70d14-171">Ha nincs megadva, nincs korlátozás.</span><span class="sxs-lookup"><span data-stu-id="70d14-171">If not specified, there is no limitation.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70d14-172">-ResourceId</span></span>
<span data-ttu-id="70d14-173">HSM-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="70d14-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-174">-Méret</span><span class="sxs-lookup"><span data-stu-id="70d14-174">-Size</span></span>
<span data-ttu-id="70d14-175">Az RSA-kulcs mérete a BITS lapon</span><span class="sxs-lookup"><span data-stu-id="70d14-175">RSA key size, in bits.</span></span>
<span data-ttu-id="70d14-176">Ha nem adja meg, akkor a szolgáltatás biztonságos alapértelmezett értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="70d14-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-177">-Címke</span><span class="sxs-lookup"><span data-stu-id="70d14-177">-Tag</span></span>
<span data-ttu-id="70d14-178">A Hashtable jelölő billentyűk.</span><span class="sxs-lookup"><span data-stu-id="70d14-178">A hashtable representing key tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d14-179">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70d14-179">-Confirm</span></span>
<span data-ttu-id="70d14-180">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70d14-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d14-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d14-181">-WhatIf</span></span>
<span data-ttu-id="70d14-182">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70d14-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70d14-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70d14-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d14-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d14-184">CommonParameters</span></span>
<span data-ttu-id="70d14-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70d14-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d14-186">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70d14-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d14-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70d14-187">INPUTS</span></span>

### <span data-ttu-id="70d14-188">Microsoft. Azure. Command. PSManagedHsm. models.</span><span class="sxs-lookup"><span data-stu-id="70d14-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="70d14-189">System. String</span><span class="sxs-lookup"><span data-stu-id="70d14-189">System.String</span></span>

## <span data-ttu-id="70d14-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70d14-190">OUTPUTS</span></span>

### <span data-ttu-id="70d14-191">Microsoft. Azure. Command. PSManagedHsm. models.</span><span class="sxs-lookup"><span data-stu-id="70d14-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="70d14-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70d14-192">NOTES</span></span>

## <span data-ttu-id="70d14-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70d14-193">RELATED LINKS</span></span>

[<span data-ttu-id="70d14-194">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="70d14-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="70d14-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="70d14-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="70d14-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="70d14-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="70d14-197">Visszavonás – AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="70d14-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="70d14-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="70d14-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="70d14-199">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="70d14-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
