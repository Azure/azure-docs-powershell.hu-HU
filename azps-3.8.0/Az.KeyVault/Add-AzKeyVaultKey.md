---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 3d0f7267d1dbe899de0e0414c52a395985f09bfd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412537"
---
# <span data-ttu-id="cbbe6-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cbbe6-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="cbbe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="cbbe6-103">Kulcsot hoz létre egy kulcstárban, vagy kulcsot importál egy kulcstárba.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="cbbe6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbbe6-104">SYNTAX</span></span>

### <span data-ttu-id="cbbe6-105">InteractiveCreate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cbbe6-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbe6-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="cbbe6-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbe6-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="cbbe6-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbe6-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="cbbe6-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbe6-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="cbbe6-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbbe6-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="cbbe6-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbbe6-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbbe6-111">DESCRIPTION</span></span>
<span data-ttu-id="cbbe6-112">Az **Add-AzKeyVaultKey** parancsmag létrehoz egy kulcsot egy kulcstárban az Azure Kulcstárban, vagy importál egy kulcsot egy kulcstárba.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="cbbe6-113">Ezzel a parancsmagkal az alábbi módszerek bármelyikével adhat hozzá billentyűket:</span><span class="sxs-lookup"><span data-stu-id="cbbe6-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="cbbe6-114">Hozzon létre egy kulcsot egy hardverbiztonsági modulban (HSM) a kulcstár szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="cbbe6-115">Termékkulcs létrehozása a kulcstár szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="cbbe6-116">Importálhat egy kulcsot a saját hardveres biztonsági modulból (HSM) a kulcstár szolgáltatásban található HSM-ekbe.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="cbbe6-117">Importálja a kulcsot egy .pfx fájlból a számítógépen.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="cbbe6-118">A kulcstár szolgáltatásban egy .pfx fájlból hardveres biztonsági modulokba (HSM-eket) importálhat.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="cbbe6-119">E műveletek bármelyikéhez meg kell adnia a legfontosabb attribútumokat, vagy el kell fogadnia az alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="cbbe6-120">Ha olyan kulcsot hoz létre vagy importál, amely neve megegyezik a kulcstárban meglévő kulcs nevével, az eredeti kulcs frissül az új kulcshoz megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="cbbe6-121">A korábbi értékeket a kulcs adott verziójához használt verzióspecifikus URI azonosítóval tudja elérni.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="cbbe6-122">A legfontosabb verziókról és az URI-struktúráról a Kulcstár REST API dokumentációjában található A kulcsok és a titkos információk szolgáltatásról olvashat. [](http://go.microsoft.com/fwlink/?linkid=518560)</span><span class="sxs-lookup"><span data-stu-id="cbbe6-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="cbbe6-123">Megjegyzés: Ha saját hardveres biztonsági modulból importálni kívánt kulcsot, először létre kell hoznia egy BYOK-csomagot (egy .byok kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészletével.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="cbbe6-124">További információt az Azure-kulcstárhoz HSM-Protected kulcsok létrehozása és [átvitele.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="cbbe6-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="cbbe6-125">Gyakorlati megoldásként a termékkulcsról a létrehozása vagy frissítése után is biztonsági Backup-AzKeyVaultKey parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="cbbe6-126">Nincs előtűnés funkció, ezért ha véletlenül törli vagy törli a kulcsot, majd meggondolja magát, a kulcs csak akkor állítható helyre, ha biztonsági másolatot készít róla.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="cbbe6-127">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbbe6-127">EXAMPLES</span></span>

### <span data-ttu-id="cbbe6-128">1. példa: Kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="cbbe6-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="cbbe6-129">Ez a parancs létrehoz egy ITSoftware nevű szoftver védett kulcsot a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="cbbe6-130">2. példa: HSM-védelemű kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="cbbe6-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="cbbe6-131">Ez a parancs létrehoz egy HSM által védett kulcsot a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="cbbe6-132">3. példa: Nem alapértelmezett értékeket tartalmazó kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="cbbe6-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="cbbe6-133">Az első parancs az értékeket visszafejti és ellenőrzi a $KeyOperations változóban.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="cbbe6-134">A második parancs a **Get-Date** parancsmag használatával létrehozza az **UTC-ben** definiált DateTime objektumot.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="cbbe6-135">Ez az objektum a jövőben két évet ad meg.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="cbbe6-136">A parancs ezt a dátumot a $Expires tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="cbbe6-137">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cbbe6-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="cbbe6-138">A harmadik parancs a **Get-Date** parancsmag használatával hoz létre **DateTime-objektumot.**</span><span class="sxs-lookup"><span data-stu-id="cbbe6-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cbbe6-139">Ez az objektum az aktuális UTC-időt adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-139">That object specifies current UTC time.</span></span> <span data-ttu-id="cbbe6-140">A parancs ezt a dátumot a $NotBefore tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="cbbe6-141">Az utolsó parancs létrehoz egy ITHsmNonDefault nevű kulcsot, amely egy HSM-védelem alatt áll.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="cbbe6-142">A parancs az engedélyezett kulcsműveleteket a $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="cbbe6-143">A parancs az előző  parancsokban létrehozott Lejárati és *NemBefore* paraméterek, valamint a magas súlyosság és az IT címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="cbbe6-144">Az új kulcs le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-144">The new key is disabled.</span></span> <span data-ttu-id="cbbe6-145">A beállítás engedélyezéséhez használja a **Set-AzKeyVaultKey** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="cbbe6-146">4. példa: HSM-védelemű kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="cbbe6-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="cbbe6-147">Ez a parancs a *KeyFilePath* paraméter által megadott helyről importálja az ITByok nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="cbbe6-148">Az importált kulcs egy HSM-védelem alatt áll.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="cbbe6-149">Ha saját hardveres biztonsági modulból importálni kívánt kulcsot, először létre kell hoznia egy BYOK-csomagot (egy .byok kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészletével.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="cbbe6-150">További információt az Azure-kulcstárhoz HSM-Protected kulcsok létrehozása és [átvitele.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="cbbe6-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="cbbe6-151">5. példa: Szoftver által védett kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="cbbe6-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="cbbe6-152">Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="cbbe6-153">További információért írja be a `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="cbbe6-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="cbbe6-154">A második parancs létrehoz egy szoftverjelszót a Contoso kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="cbbe6-155">A parancs megadja a kulcs és a jelszó helyét a $Password.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="cbbe6-156">6. példa: Kulcs importálása és attribútumok hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="cbbe6-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="cbbe6-157">Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="cbbe6-158">A második parancs a **Get-Date** parancsmag használatával **dateTime** objektumot hoz létre, majd az objektumot a $Expires tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="cbbe6-159">A harmadik parancs létrehozza a $tags változót a nagy súlyosságú és az it-it-címkék beállítására.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="cbbe6-160">A végleges parancs egy kulcsot HSM-kulcsként importál a megadott helyről.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="cbbe6-161">A parancs megadja a $Expires és a $Password-ban tárolt jelszóban tárolt lejárati időt, és alkalmazza a $tags.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="cbbe6-162">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbbe6-162">PARAMETERS</span></span>

### <span data-ttu-id="cbbe6-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbbe6-163">-DefaultProfile</span></span>
<span data-ttu-id="cbbe6-164">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cbbe6-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbbe6-165">-Destination</span><span class="sxs-lookup"><span data-stu-id="cbbe6-165">-Destination</span></span>
<span data-ttu-id="cbbe6-166">Megadja, hogy a kulcs hozzáadva legyen-e szoftveres vagy HSM által védett kulcsként a kulcstár szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="cbbe6-167">Érvényes értékek: HSM és Software.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="cbbe6-168">Megjegyzés: Ahhoz, hogy a HSM-et használni tudja célként, olyan kulcstárat kell használnia, amely támogatja a HSM-eket.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="cbbe6-169">Az Azure Key Vault szolgáltatásszintjéről és funkcióiról az [Azure Key Vault árazási](http://go.microsoft.com/fwlink/?linkid=512521)webhelyén talál további információt.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="cbbe6-170">Új kulcs létrehozásakor ez a paraméter szükséges.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="cbbe6-171">Ha a *KeyFilePath* paraméterrel importál egy kulcsot, a paraméter megadása nem kötelező:</span><span class="sxs-lookup"><span data-stu-id="cbbe6-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="cbbe6-172">Ha nem adja meg ezt a paramétert, és ez a parancsmag egy .byok fájlnévkiterjesztésű kulcsot importál, akkor a kulcsot HSM-védelem alatt lévő kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="cbbe6-173">A parancsmag nem tudja importálni a kulcsot szoftver által védett kulcsként.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="cbbe6-174">Ha nem adja meg ezt a paramétert, és ez a parancsmag egy .pfx fájlnévkiterjesztésű kulcsot importál, a kulcsot szoftvervédelem alatt lévő kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="cbbe6-175">-Disable</span><span class="sxs-lookup"><span data-stu-id="cbbe6-175">-Disable</span></span>
<span data-ttu-id="cbbe6-176">Azt jelzi, hogy a hozzáadott kulcs a letiltás kezdeti állapotára van állítva.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="cbbe6-177">A kulcs használatára tett minden kísérlet sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="cbbe6-178">Akkor használja ezt a paramétert, ha előre betölti a később engedélyezni kívánt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="cbbe6-179">-Lejár</span><span class="sxs-lookup"><span data-stu-id="cbbe6-179">-Expires</span></span>
<span data-ttu-id="cbbe6-180">A parancsmag által adott kulcs **Lejárati** idejét adja meg DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="cbbe6-181">Ez a paraméter egyezményes világidőt (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cbbe6-182">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cbbe6-183">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cbbe6-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="cbbe6-184">Ha nem adja meg ezt a paramétert, a kulcs nem jár le.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="cbbe6-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbbe6-185">-InputObject</span></span>
<span data-ttu-id="cbbe6-186">Tárolóobjektum.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-186">Vault object.</span></span>

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

### <span data-ttu-id="cbbe6-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="cbbe6-187">-KeyFilePassword</span></span>
<span data-ttu-id="cbbe6-188">Az importált fájl jelszavát adja meg **SecureString objektumként.**</span><span class="sxs-lookup"><span data-stu-id="cbbe6-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="cbbe6-189">A **SecureString objektum** beszerzéséhez használja a **ConvertTo-SecureString** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="cbbe6-190">További információért írja be a `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="cbbe6-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="cbbe6-191">A .pfx kiterjesztésű fájlok importálásához meg kell adnia ezt a jelszót.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="cbbe6-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="cbbe6-192">-KeyFilePath</span></span>
<span data-ttu-id="cbbe6-193">Egy olyan helyi fájl elérési útját adja meg, amely a parancsmag által importálni kívánt fontos anyagot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="cbbe6-194">Az érvényes fájlnévkiterjesztések a .byok és a .pfx.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="cbbe6-195">Ha a fájl .byok fájl, a kulcs az importálás után automatikusan az HSM-ekkel lesz védve, és ez az alapértelmezett beállítás nem bírálható felül.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="cbbe6-196">Ha a fájl .pfx fájl, a kulcsot az importálás után automatikusan szoftver védi.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="cbbe6-197">Az alapértelmezett beállítás felülbírálása érdekében állítsa a Cél paramétert HSM-nek, hogy a kulcs HSM-védelem alatt ússa meg. </span><span class="sxs-lookup"><span data-stu-id="cbbe6-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="cbbe6-198">Ha megadja ezt a paramétert, a *Cél* paraméter megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="cbbe6-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="cbbe6-199">-KeyOps</span></span>
<span data-ttu-id="cbbe6-200">A parancsmag által hozzáadható billentyűvel elvégezhető műveletek tömbje.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="cbbe6-201">Ha nem adja meg ezt a paramétert, az összes művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="cbbe6-202">A paraméter elfogadható értékei a [JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300)specifikációban meghatározott kulcsműveletek vesszővel elválasztott listája:</span><span class="sxs-lookup"><span data-stu-id="cbbe6-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="cbbe6-203">Titkosítás</span><span class="sxs-lookup"><span data-stu-id="cbbe6-203">Encrypt</span></span>
- <span data-ttu-id="cbbe6-204">Visszafejtése</span><span class="sxs-lookup"><span data-stu-id="cbbe6-204">Decrypt</span></span>
- <span data-ttu-id="cbbe6-205">Sortörés</span><span class="sxs-lookup"><span data-stu-id="cbbe6-205">Wrap</span></span>
- <span data-ttu-id="cbbe6-206">Unwrap</span><span class="sxs-lookup"><span data-stu-id="cbbe6-206">Unwrap</span></span>
- <span data-ttu-id="cbbe6-207">Aláírás</span><span class="sxs-lookup"><span data-stu-id="cbbe6-207">Sign</span></span>
- <span data-ttu-id="cbbe6-208">Ellenőrzés</span><span class="sxs-lookup"><span data-stu-id="cbbe6-208">Verify</span></span>

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

### <span data-ttu-id="cbbe6-209">-Name</span><span class="sxs-lookup"><span data-stu-id="cbbe6-209">-Name</span></span>
<span data-ttu-id="cbbe6-210">A kulcstárhoz hozzáadni megfelelő kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="cbbe6-211">Ez a parancsmag egy kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstár neve és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="cbbe6-212">A névnek egy 1 és 63 karakter hosszúságú karakterláncnak kell lennie, amely csak 0-9, a-z, A-Z és - (kötőjelet) tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="cbbe6-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="cbbe6-213">-NotBefore</span></span>
<span data-ttu-id="cbbe6-214">Azt az időt adja meg **DateTime-objektumként,** amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="cbbe6-215">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-215">This parameter uses UTC.</span></span> <span data-ttu-id="cbbe6-216">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cbbe6-217">Ha nem adja meg ezt a paramétert, a kulcs azonnal használható.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="cbbe6-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbbe6-218">-ResourceId</span></span>
<span data-ttu-id="cbbe6-219">Tároló erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="cbbe6-220">-Size</span><span class="sxs-lookup"><span data-stu-id="cbbe6-220">-Size</span></span>
<span data-ttu-id="cbbe6-221">RSA-billentyű mérete bitben.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-221">RSA key size, in bits.</span></span> <span data-ttu-id="cbbe6-222">Ha nincs megadva, a szolgáltatás biztonságos alapértelmezett beállítást biztosít.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-222">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="cbbe6-223">-Tag</span><span class="sxs-lookup"><span data-stu-id="cbbe6-223">-Tag</span></span>
<span data-ttu-id="cbbe6-224">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cbbe6-225">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="cbbe6-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cbbe6-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cbbe6-226">-VaultName</span></span>
<span data-ttu-id="cbbe6-227">Annak a kulcstárnak a nevét adja meg, amelyhez ez a parancsmag hozzáadja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="cbbe6-228">Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="cbbe6-229">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbbe6-229">-Confirm</span></span>
<span data-ttu-id="cbbe6-230">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbbe6-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbbe6-231">-WhatIf</span></span>
<span data-ttu-id="cbbe6-232">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbbe6-233">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbbe6-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbbe6-234">CommonParameters</span></span>
<span data-ttu-id="cbbe6-235">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbbe6-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbbe6-236">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbbe6-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbbe6-237">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbbe6-237">INPUTS</span></span>

### <span data-ttu-id="cbbe6-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cbbe6-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cbbe6-239">System.String</span><span class="sxs-lookup"><span data-stu-id="cbbe6-239">System.String</span></span>

## <span data-ttu-id="cbbe6-240">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbbe6-240">OUTPUTS</span></span>

### <span data-ttu-id="cbbe6-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cbbe6-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="cbbe6-242">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbbe6-242">NOTES</span></span>

## <span data-ttu-id="cbbe6-243">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbbe6-243">RELATED LINKS</span></span>

[<span data-ttu-id="cbbe6-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cbbe6-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="cbbe6-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cbbe6-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="cbbe6-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cbbe6-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

