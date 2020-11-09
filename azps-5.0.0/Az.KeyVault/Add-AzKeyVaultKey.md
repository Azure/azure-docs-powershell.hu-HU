---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 8583a078e12be5da3a6bcbbe16bc3349f51b9bdb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296888"
---
# <span data-ttu-id="848cf-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="848cf-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="848cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="848cf-102">SYNOPSIS</span></span>
<span data-ttu-id="848cf-103">Billentyűt hoz létre a fő tárolóban, vagy egy kulcsot egy fő boltozatba importál.</span><span class="sxs-lookup"><span data-stu-id="848cf-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="848cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="848cf-104">SYNTAX</span></span>

### <span data-ttu-id="848cf-105">InteractiveCreate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="848cf-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848cf-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="848cf-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848cf-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="848cf-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848cf-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="848cf-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848cf-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="848cf-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848cf-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="848cf-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="848cf-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="848cf-111">DESCRIPTION</span></span>
<span data-ttu-id="848cf-112">Az **Add-AzKeyVaultKey** parancsmag egy billentyűt hoz létre az Azure Key Vault-ban, vagy egy kulcsot importál egy fő boltozatba.</span><span class="sxs-lookup"><span data-stu-id="848cf-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="848cf-113">Ezzel a parancsmaggal a következő módszerekkel adhat hozzá kulcsokat:</span><span class="sxs-lookup"><span data-stu-id="848cf-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="848cf-114">Hozzon létre egy kulcsot egy hardveres biztonsági modulban (HSM) a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="848cf-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="848cf-115">Kulcsot hozhat létre a szoftverben a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="848cf-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="848cf-116">Importáljon egy kulcsot a saját hardver biztonsági modulból (HSM) a HSM a Key Vault szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="848cf-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="848cf-117">Importáljon egy kulcsot egy. pfx fájlból a számítógépre.</span><span class="sxs-lookup"><span data-stu-id="848cf-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="848cf-118">Importáljon egy kulcsot egy. pfx fájlból a számítógépen a hardver biztonsági moduljaihoz (HSM) a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="848cf-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="848cf-119">A fenti műveletek bármelyikével alapvető attribútumokat adhat meg, illetve elfogadhat alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="848cf-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="848cf-120">Ha olyan billentyűt hoz létre vagy importál, amelynek a neve megegyezik egy meglévő kulccsal, az eredeti kulcs frissül az új kulcshoz megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="848cf-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="848cf-121">A korábbi értékeket a kulcs adott verziójához tartozó, a verziószámot tartalmazó URI-azonosító használatával érheti el.</span><span class="sxs-lookup"><span data-stu-id="848cf-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="848cf-122">A főbb verziókkal és az URI-felépítéssel kapcsolatban további információt a [kulcsok és titkok](http://go.microsoft.com/fwlink/?linkid=518560) a Key Vault REST API-dokumentációban című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="848cf-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="848cf-123">Megjegyzés: Ha egy kulcsot saját hardveres biztonsági modulból szeretne importálni, először létre kell hoznia egy BYOK-csomagot (. BYOK fájlnév-kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészlet használatával.</span><span class="sxs-lookup"><span data-stu-id="848cf-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="848cf-124">További információt a [HSM-Protected kulcsok létrehozása és továbbítása az Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252)-ban című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="848cf-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="848cf-125">Ajánlott eljárásként készítsen biztonsági másolatot a kulcsról, miután létrehozta vagy frissíti őket a Backup-AzKeyVaultKey parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="848cf-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="848cf-126">Nincs eltávolítási funkció, ezért ha véletlenül törli a billentyűt vagy törli, majd meggondolja magát, a kulcs nem állítható helyre, hacsak nem rendelkezik biztonsági másolattal.</span><span class="sxs-lookup"><span data-stu-id="848cf-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="848cf-127">Példák</span><span class="sxs-lookup"><span data-stu-id="848cf-127">EXAMPLES</span></span>

### <span data-ttu-id="848cf-128">Példa 1: kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="848cf-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="848cf-129">Ez a parancs létrehoz egy ITSoftware nevű, a contoso nevű kulcsfájl nevű kulccsal védett kulcsot.</span><span class="sxs-lookup"><span data-stu-id="848cf-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="848cf-130">2. példa: HSM-védelemmel ellátott kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="848cf-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="848cf-131">Ez a parancs egy HSM-védelemmel ellátott billentyűt hoz létre a contoso nevű kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="848cf-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="848cf-132">3. példa: kulcs létrehozása nem alapértelmezett értékekkel</span><span class="sxs-lookup"><span data-stu-id="848cf-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="848cf-133">Az első parancs a $KeyOperations változóban tárolja az értékeket dekódolja és ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="848cf-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="848cf-134">A második parancs létrehoz egy **datetime** típusú objektumot, amelyet az UTC a **Get-Date** parancsmag használatával definiál.</span><span class="sxs-lookup"><span data-stu-id="848cf-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="848cf-135">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="848cf-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="848cf-136">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="848cf-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="848cf-137">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="848cf-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="848cf-138">A harmadik parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="848cf-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="848cf-139">Az objektum a jelenlegi UTC időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="848cf-139">That object specifies current UTC time.</span></span> <span data-ttu-id="848cf-140">A parancs a $NotBefore változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="848cf-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="848cf-141">A végleges parancs létrehoz egy ITHsmNonDefault, amely egy HSM-védelemmel ellátott kulcs.</span><span class="sxs-lookup"><span data-stu-id="848cf-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="848cf-142">A parancs a $KeyOperations tárolt, engedélyezett műveletek értékeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="848cf-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="848cf-143">A parancs az előző parancsokban létrehozott *lejáratok* és *NotBefore* paramétereinek időpontját adja meg, valamint a nagy SÚLYOSSÁGú és az IT-címkéket.</span><span class="sxs-lookup"><span data-stu-id="848cf-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="848cf-144">Az új kulcs le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="848cf-144">The new key is disabled.</span></span> <span data-ttu-id="848cf-145">A **set-AzKeyVaultKey** parancsmag használatával engedélyezheti azt.</span><span class="sxs-lookup"><span data-stu-id="848cf-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="848cf-146">Példa 4: HSM-védelemmel ellátott kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="848cf-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="848cf-147">Ez a parancs a ITByok nevű kulcsot a *KeyFilePath* paraméter által megadott helyről importálja.</span><span class="sxs-lookup"><span data-stu-id="848cf-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="848cf-148">Az importált kulcs egy HSM-védelemmel ellátott kulcs.</span><span class="sxs-lookup"><span data-stu-id="848cf-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="848cf-149">Ha egy kulcsot saját hardveres biztonsági modulból szeretne importálni, először létre kell hoznia egy BYOK-csomagot (. BYOK fájlnév-kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészlet használatával.</span><span class="sxs-lookup"><span data-stu-id="848cf-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="848cf-150">További információt a [HSM-Protected kulcsok létrehozása és továbbítása az Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252)-ban című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="848cf-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="848cf-151">Példa 5: szoftverrel védett kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="848cf-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="848cf-152">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="848cf-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="848cf-153">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="848cf-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="848cf-154">A második parancs a contoso Key Vault-ban hozza létre a szoftverhez tartozó jelszót.</span><span class="sxs-lookup"><span data-stu-id="848cf-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="848cf-155">A parancs a $Passwordban tárolt kulcs és jelszó helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="848cf-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="848cf-156">6. példa: kulcs importálása és attribútumok hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="848cf-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="848cf-157">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="848cf-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="848cf-158">A második parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával, majd az objektumot az $Expires változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="848cf-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="848cf-159">A harmadik parancs a $tags változót hozza létre a nagy súlyosságú és a címkék beállításához.</span><span class="sxs-lookup"><span data-stu-id="848cf-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="848cf-160">A végleges parancs a megadott helyről importálja a kulcsot a HSM-kulcsként.</span><span class="sxs-lookup"><span data-stu-id="848cf-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="848cf-161">A parancs a $Password tárolt $Expires és jelszóban tárolt elévülési időt adja meg, és a $tagsban tárolt címkéket alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="848cf-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="848cf-162">7. példa: kulcsos kulcscsere-kulcs (KEK) létrehozása a "saját kulcs" (BYOK) funkcióhoz</span><span class="sxs-lookup"><span data-stu-id="848cf-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="848cf-163">Kulcsot hoz létre (a továbbiakban: kulcs Exchange-kulcs (KEK)).</span><span class="sxs-lookup"><span data-stu-id="848cf-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="848cf-164">A KEK-nek olyan RSA-HSM-kulcsnak kell lennie, amely csak az importálási kulcs művelettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="848cf-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="848cf-165">Csak a Key Vault Premium SKU támogatja az RSA-HSM-kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="848cf-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="848cf-166">További részletekért olvassa el a https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="848cf-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="848cf-167">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="848cf-167">PARAMETERS</span></span>

### <span data-ttu-id="848cf-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848cf-168">-DefaultProfile</span></span>
<span data-ttu-id="848cf-169">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="848cf-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="848cf-170">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="848cf-170">-Destination</span></span>
<span data-ttu-id="848cf-171">Itt adhatja meg, hogy a kulcsot szoftverrel védett kulcsként vagy HSM-védelemmel ellátott kulccsal szeretné-e hozzáadni a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="848cf-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="848cf-172">Érvényes értékek: HSM és szoftver.</span><span class="sxs-lookup"><span data-stu-id="848cf-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="848cf-173">Megjegyzés: Ha a HSM-t célként szeretné használni, rendelkeznie kell a HSM támogató fő tárolóval.</span><span class="sxs-lookup"><span data-stu-id="848cf-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="848cf-174">Az Azure Key Vault szolgáltatás szintjeiről és képességeiről további információt az [Azure Key Vault árképzési webhelyén](http://go.microsoft.com/fwlink/?linkid=512521)találhat.</span><span class="sxs-lookup"><span data-stu-id="848cf-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="848cf-175">Ezt a paramétert új kulcs létrehozásakor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="848cf-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="848cf-176">Ha a *KeyFilePath* paraméterrel importál egy billentyűt, akkor ez a paraméter nem kötelező:</span><span class="sxs-lookup"><span data-stu-id="848cf-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="848cf-177">Ha nem adja meg ezt a paramétert, és ez a parancsmag olyan kulcsot importál, amely. byok fájlnév-kiterjesztéssel rendelkezik, a kulcsot HSM-védelemmel ellátott kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="848cf-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="848cf-178">A parancsmag nem tudja importálni a kulcsot szoftveres védelemmel ellátott kulcsként.</span><span class="sxs-lookup"><span data-stu-id="848cf-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="848cf-179">Ha nem adja meg ezt a paramétert, és ez a parancsmag a. pfx fájlnév-kiterjesztésű kulcsot importálja, az a kulcsot szoftveres védelemmel ellátott kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="848cf-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="848cf-180">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="848cf-180">-Disable</span></span>
<span data-ttu-id="848cf-181">Azt jelzi, hogy a felvenni kívánt kulcs a letiltott állapotú eredeti állapotra van állítva.</span><span class="sxs-lookup"><span data-stu-id="848cf-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="848cf-182">A billentyű használatát minden próbálkozás sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="848cf-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="848cf-183">Akkor használja ezt a paramétert, ha előre betöltődik a később engedélyezni kívánt billentyűk.</span><span class="sxs-lookup"><span data-stu-id="848cf-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="848cf-184">-Lejár</span><span class="sxs-lookup"><span data-stu-id="848cf-184">-Expires</span></span>
<span data-ttu-id="848cf-185">A lejárati idő **datetime** objektumként való megadása a parancsmag által hozzáadott kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="848cf-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="848cf-186">Ez a paraméter koordinált univerzális időpontot (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="848cf-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="848cf-187">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="848cf-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="848cf-188">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="848cf-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="848cf-189">Ha nem adja meg ezt a paramétert, a kulcs nem jár le.</span><span class="sxs-lookup"><span data-stu-id="848cf-189">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="848cf-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="848cf-190">-InputObject</span></span>
<span data-ttu-id="848cf-191">Boltozat objektum.</span><span class="sxs-lookup"><span data-stu-id="848cf-191">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="848cf-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="848cf-192">-KeyFilePassword</span></span>
<span data-ttu-id="848cf-193">Az importált fájlhoz tartozó jelszót **SecureString** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="848cf-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="848cf-194">**SecureString** objektum beolvasásához használja a **ConvertTo-SecureString** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="848cf-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="848cf-195">További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="848cf-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="848cf-196">A. pfx fájlnév-kiterjesztésű fájlok importálásához meg kell adnia ezt a jelszót.</span><span class="sxs-lookup"><span data-stu-id="848cf-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="848cf-197">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="848cf-197">-KeyFilePath</span></span>
<span data-ttu-id="848cf-198">A parancsmag által importált fontos anyagot tartalmazó helyi fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="848cf-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="848cf-199">Az érvényes fájlnév-kiterjesztések. byok és. pfx.</span><span class="sxs-lookup"><span data-stu-id="848cf-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="848cf-200">Ha a fájl. byok fájl, az importálás után a rendszer automatikusan védi a kulcsot, és nem tudja felülírni ezt az alapértelmezett HSM.</span><span class="sxs-lookup"><span data-stu-id="848cf-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="848cf-201">Ha a fájl. pfx fájl, a kulcs automatikusan védett a szoftverrel az importálás után.</span><span class="sxs-lookup"><span data-stu-id="848cf-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="848cf-202">Az alapértelmezett beállítás felülbírálásához állítsa a *cél* paramétert a HSM értékre, hogy a kulcs HSM-védelemmel legyen ellátva.</span><span class="sxs-lookup"><span data-stu-id="848cf-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="848cf-203">Ha ezt a paramétert adja meg, a *cél* paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="848cf-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="848cf-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="848cf-204">-KeyOps</span></span>
<span data-ttu-id="848cf-205">Megadja azokat a műveleteket, amelyeket a parancsmag által hozzáadott kulccsal végezhet el.</span><span class="sxs-lookup"><span data-stu-id="848cf-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="848cf-206">Ha nem adja meg ezt a paramétert, akkor az összes művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="848cf-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="848cf-207">A paraméter elfogadható értékei: a [JSON-webkulcs (JWK) specifikációja](http://go.microsoft.com/fwlink/?LinkID=613300)által meghatározott főbb műveletek vesszővel elválasztott listája:</span><span class="sxs-lookup"><span data-stu-id="848cf-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="848cf-208">beavatkozik</span><span class="sxs-lookup"><span data-stu-id="848cf-208">encrypt</span></span>
- <span data-ttu-id="848cf-209">visszafejtése</span><span class="sxs-lookup"><span data-stu-id="848cf-209">decrypt</span></span>
- <span data-ttu-id="848cf-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="848cf-210">wrapKey</span></span>
- <span data-ttu-id="848cf-211">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="848cf-211">unwrapKey</span></span>
- <span data-ttu-id="848cf-212">jel</span><span class="sxs-lookup"><span data-stu-id="848cf-212">sign</span></span>
- <span data-ttu-id="848cf-213">Ellenőrizze</span><span class="sxs-lookup"><span data-stu-id="848cf-213">verify</span></span>
- <span data-ttu-id="848cf-214">Importálás (csak KEK esetén: 7. példa)</span><span class="sxs-lookup"><span data-stu-id="848cf-214">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="848cf-215">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="848cf-215">-Name</span></span>
<span data-ttu-id="848cf-216">Annak a kulcsnak a nevét adja meg, amelyet fel szeretne venni a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="848cf-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="848cf-217">Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="848cf-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="848cf-218">A névnek 0-9 csak az 1-es, a-z, A-z és A-(a kötőjel szimbólumot) tartalmazó 63-karakterből kell állnia.</span><span class="sxs-lookup"><span data-stu-id="848cf-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="848cf-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="848cf-219">-NotBefore</span></span>
<span data-ttu-id="848cf-220">Itt adhatja meg az időt **datetime** objektumként, amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="848cf-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="848cf-221">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="848cf-221">This parameter uses UTC.</span></span> <span data-ttu-id="848cf-222">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="848cf-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="848cf-223">Ha nem adja meg ezt a paramétert, akkor a billentyű azonnal használható.</span><span class="sxs-lookup"><span data-stu-id="848cf-223">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="848cf-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="848cf-224">-ResourceId</span></span>
<span data-ttu-id="848cf-225">Vault-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="848cf-225">Vault Resource Id.</span></span>

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

### <span data-ttu-id="848cf-226">-Méret</span><span class="sxs-lookup"><span data-stu-id="848cf-226">-Size</span></span>
<span data-ttu-id="848cf-227">Az RSA-kulcs mérete a BITS lapon</span><span class="sxs-lookup"><span data-stu-id="848cf-227">RSA key size, in bits.</span></span> <span data-ttu-id="848cf-228">Ha nem adja meg, akkor a szolgáltatás biztonságos alapértelmezett értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="848cf-228">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="848cf-229">-Címke</span><span class="sxs-lookup"><span data-stu-id="848cf-229">-Tag</span></span>
<span data-ttu-id="848cf-230">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="848cf-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="848cf-231">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="848cf-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="848cf-232">-VaultName</span><span class="sxs-lookup"><span data-stu-id="848cf-232">-VaultName</span></span>
<span data-ttu-id="848cf-233">Annak a kulcsnak a nevét adja meg, amelyre a parancsmag hozzáadja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="848cf-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="848cf-234">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="848cf-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="848cf-235">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="848cf-235">-Confirm</span></span>
<span data-ttu-id="848cf-236">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="848cf-236">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="848cf-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="848cf-237">-WhatIf</span></span>
<span data-ttu-id="848cf-238">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="848cf-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="848cf-239">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="848cf-239">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="848cf-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848cf-240">CommonParameters</span></span>
<span data-ttu-id="848cf-241">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="848cf-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848cf-242">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="848cf-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848cf-243">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="848cf-243">INPUTS</span></span>

### <span data-ttu-id="848cf-244">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="848cf-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="848cf-245">System. String</span><span class="sxs-lookup"><span data-stu-id="848cf-245">System.String</span></span>

## <span data-ttu-id="848cf-246">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="848cf-246">OUTPUTS</span></span>

### <span data-ttu-id="848cf-247">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="848cf-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="848cf-248">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="848cf-248">NOTES</span></span>

## <span data-ttu-id="848cf-249">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="848cf-249">RELATED LINKS</span></span>

[<span data-ttu-id="848cf-250">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="848cf-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="848cf-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="848cf-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="848cf-252">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="848cf-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="848cf-253">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="848cf-253">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
