---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 61125ae7d9fa78ec9f121cc9b60610258ad2c67c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405397"
---
# <span data-ttu-id="e7faa-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7faa-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="e7faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7faa-102">SYNOPSIS</span></span>
<span data-ttu-id="e7faa-103">Kulcsot hoz létre egy kulcstárban, vagy kulcsot importál egy kulcstárba.</span><span class="sxs-lookup"><span data-stu-id="e7faa-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="e7faa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7faa-104">SYNTAX</span></span>

### <span data-ttu-id="e7faa-105">InteractiveCreate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7faa-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="e7faa-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="e7faa-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="e7faa-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="e7faa-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="e7faa-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="e7faa-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="e7faa-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7faa-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="e7faa-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="e7faa-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="e7faa-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7faa-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="e7faa-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7faa-117">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7faa-117">DESCRIPTION</span></span>
<span data-ttu-id="e7faa-118">Az **Add-AzKeyVaultKey** parancsmag létrehoz egy kulcsot egy kulcstárban az Azure Kulcstárban, vagy importál egy kulcsot egy kulcstárba.</span><span class="sxs-lookup"><span data-stu-id="e7faa-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="e7faa-119">Ezzel a parancsmagkal az alábbi módszerek bármelyikével adhat hozzá billentyűket:</span><span class="sxs-lookup"><span data-stu-id="e7faa-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="e7faa-120">Hozzon létre egy kulcsot egy hardveres biztonsági modulban (HSM) a kulcstár szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e7faa-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="e7faa-121">Termékkulcs létrehozása a kulcstár szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e7faa-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="e7faa-122">Importálhat egy kulcsot a saját hardveres biztonsági modulból (HSM) a kulcstár szolgáltatásban található HSM-ekbe.</span><span class="sxs-lookup"><span data-stu-id="e7faa-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="e7faa-123">Importálja a kulcsot egy .pfx fájlból a számítógépen.</span><span class="sxs-lookup"><span data-stu-id="e7faa-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="e7faa-124">A kulcstár szolgáltatásban egy .pfx fájlból hardveres biztonsági modulokba (HSM-eket) importálhat.</span><span class="sxs-lookup"><span data-stu-id="e7faa-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="e7faa-125">E műveletek bármelyikéhez meg kell adnia a legfontosabb attribútumokat, vagy el kell fogadnia az alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="e7faa-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="e7faa-126">Ha olyan kulcsot hoz létre vagy importál, amely neve megegyezik a kulcstárban meglévő kulcs nevével, az eredeti kulcs frissül az új kulcshoz megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="e7faa-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="e7faa-127">A korábbi értékeket a kulcs adott verziójához használt verzióspecifikus URI azonosítóval tudja elérni.</span><span class="sxs-lookup"><span data-stu-id="e7faa-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="e7faa-128">A legfontosabb verziókról és az URI-struktúráról a Kulcstár REST API dokumentációjában található A kulcsok és a titkos információk szolgáltatásról olvashat. [](http://go.microsoft.com/fwlink/?linkid=518560)</span><span class="sxs-lookup"><span data-stu-id="e7faa-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="e7faa-129">Megjegyzés: Ha saját hardveres biztonsági modulból importálni kívánt kulcsot, először létre kell hoznia egy BYOK-csomagot (egy .byok kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészletével.</span><span class="sxs-lookup"><span data-stu-id="e7faa-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="e7faa-130">További információt az Azure-kulcstárhoz HSM-Protected kulcsok létrehozása és [átvitele.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="e7faa-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="e7faa-131">Gyakorlati megoldásként a termékkulcsról a létrehozása vagy frissítése után is biztonsági Backup-AzKeyVaultKey parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e7faa-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="e7faa-132">Nincs előtűnés funkció, ezért ha véletlenül törli vagy törli a kulcsot, majd meggondolja magát, a kulcs csak akkor állítható helyre, ha biztonsági másolatot készít róla.</span><span class="sxs-lookup"><span data-stu-id="e7faa-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="e7faa-133">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7faa-133">EXAMPLES</span></span>

### <span data-ttu-id="e7faa-134">1. példa: Kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7faa-134">Example 1: Create a key</span></span>
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

<span data-ttu-id="e7faa-135">Ez a parancs létrehoz egy ITSoftware nevű szoftver védett kulcsot a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="e7faa-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="e7faa-136">2. példa: HSM-védelemű kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7faa-136">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="e7faa-137">Ez a parancs létrehoz egy HSM által védett kulcsot a Contoso nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="e7faa-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="e7faa-138">3. példa: Nem alapértelmezett értékeket tartalmazó kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7faa-138">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="e7faa-139">Az első parancs az értékeket visszafejti és ellenőrzi a $KeyOperations változóban.</span><span class="sxs-lookup"><span data-stu-id="e7faa-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="e7faa-140">A második parancs a **Get-Date** parancsmag használatával létrehozza az **UTC-ben** definiált DateTime objektumot.</span><span class="sxs-lookup"><span data-stu-id="e7faa-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e7faa-141">Ez az objektum a jövőben két évet ad meg.</span><span class="sxs-lookup"><span data-stu-id="e7faa-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="e7faa-142">A parancs ezt a dátumot a $Expires tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="e7faa-143">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e7faa-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="e7faa-144">A harmadik parancs a **Get-Date** parancsmag használatával hoz létre **DateTime-objektumot.**</span><span class="sxs-lookup"><span data-stu-id="e7faa-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e7faa-145">Ez az objektum az aktuális UTC-időt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7faa-145">That object specifies current UTC time.</span></span> <span data-ttu-id="e7faa-146">A parancs ezt a dátumot a $NotBefore tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="e7faa-147">Az utolsó parancs létrehoz egy ITHsmNonDefault nevű kulcsot, amely egy HSM-védelem alatt áll.</span><span class="sxs-lookup"><span data-stu-id="e7faa-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="e7faa-148">A parancs az engedélyezett kulcsműveleteket a $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="e7faa-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="e7faa-149">A parancs az előző  parancsokban létrehozott Lejárati és *NemBefore* paraméterek, valamint a magas súlyosság és az IT címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7faa-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="e7faa-150">Az új kulcs le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="e7faa-150">The new key is disabled.</span></span> <span data-ttu-id="e7faa-151">A beállítás engedélyezéséhez használja a **Set-AzKeyVaultKey** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7faa-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="e7faa-152">4. példa: HSM-védelemű kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="e7faa-152">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="e7faa-153">Ez a parancs a *KeyFilePath* paraméter által megadott helyről importálja az ITByok nevű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="e7faa-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="e7faa-154">Az importált kulcs egy HSM-védelem alatt áll.</span><span class="sxs-lookup"><span data-stu-id="e7faa-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="e7faa-155">Ha saját hardveres biztonsági modulból importálni kívánt kulcsot, először létre kell hoznia egy BYOK-csomagot (egy .byok kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészletével.</span><span class="sxs-lookup"><span data-stu-id="e7faa-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="e7faa-156">További információt az Azure-kulcstárhoz HSM-Protected kulcsok létrehozása és [átvitele.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="e7faa-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="e7faa-157">5. példa: Szoftver által védett kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="e7faa-157">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="e7faa-158">Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="e7faa-159">További információért írja be a `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e7faa-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="e7faa-160">A második parancs létrehoz egy szoftverjelszót a Contoso kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="e7faa-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="e7faa-161">A parancs a kulcs és a jelszó helyét adja meg a $Password.</span><span class="sxs-lookup"><span data-stu-id="e7faa-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="e7faa-162">6. példa: Kulcs importálása és attribútumok hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="e7faa-162">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="e7faa-163">Az első parancs biztonságos karakterláncgé alakít egy karakterláncot a **ConvertTo-SecureString** parancsmag használatával, majd a karakterláncot a $Password tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="e7faa-164">A második parancs a **Get-Date** parancsmag használatával **dateTime** objektumot hoz létre, majd az objektumot a $Expires tárolja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="e7faa-165">A harmadik parancs létrehozza a $tags változót a nagy súlyosságú és az it-it-címkék beállítására.</span><span class="sxs-lookup"><span data-stu-id="e7faa-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="e7faa-166">A végleges parancs egy kulcsot HSM-kulcsként importál a megadott helyről.</span><span class="sxs-lookup"><span data-stu-id="e7faa-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="e7faa-167">A parancs megadja a $Expires és a $Password-ban tárolt jelszóban tárolt lejárati időt, és alkalmazza a $tags.</span><span class="sxs-lookup"><span data-stu-id="e7faa-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="e7faa-168">7. példa: Kulcs exchange-kulcs (KEK) létrehozása a "hozza el a saját kulcsát" (BYOK) funkcióhoz</span><span class="sxs-lookup"><span data-stu-id="e7faa-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="e7faa-169">Létrehoz egy kulcsot (más néven kulcs exchange-kulcsot ).</b0></span><span class="sxs-lookup"><span data-stu-id="e7faa-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="e7faa-170">A KEK-nek olyan RSA-HSM kulcsnak kell lennie, amely csak az importálási kulcsművelettel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e7faa-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="e7faa-171">Csak a kulcstár prémium termékváltozata támogatja az RSA-HSM kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="e7faa-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="e7faa-172">További részletekért lásd: https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="e7faa-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="e7faa-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7faa-173">PARAMETERS</span></span>

### <span data-ttu-id="e7faa-174">-CurveName</span><span class="sxs-lookup"><span data-stu-id="e7faa-174">-CurveName</span></span>
<span data-ttu-id="e7faa-175">A három ponttal megadott görbe titkosításának görbenevét adja meg. Ez az érték akkor érvényes, ha a KeyType értéke EC.</span><span class="sxs-lookup"><span data-stu-id="e7faa-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7faa-176">-DefaultProfile</span></span>
<span data-ttu-id="e7faa-177">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e7faa-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7faa-178">-Destination</span><span class="sxs-lookup"><span data-stu-id="e7faa-178">-Destination</span></span>
<span data-ttu-id="e7faa-179">Azt adja meg, hogy a kulcsot hozzá kell-e adni szoftverrel védett kulcsként vagy HSM által védett kulcsként a kulcstár szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e7faa-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="e7faa-180">Érvényes értékek: HSM és Software.</span><span class="sxs-lookup"><span data-stu-id="e7faa-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="e7faa-181">Megjegyzés: Ha a HSM-et használnia kell célként, olyan kulcstárat kell használnia, amely támogatja a HSM-eket.</span><span class="sxs-lookup"><span data-stu-id="e7faa-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="e7faa-182">Az Azure Key Vault szolgáltatásszintjéről és funkcióiról az [Azure Key Vault árazási](http://go.microsoft.com/fwlink/?linkid=512521)webhelyén talál további információt.</span><span class="sxs-lookup"><span data-stu-id="e7faa-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="e7faa-183">Új kulcs létrehozásakor ez a paraméter szükséges.</span><span class="sxs-lookup"><span data-stu-id="e7faa-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="e7faa-184">Ha a *KeyFilePath* paraméterrel importál egy kulcsot, a paraméter megadása nem kötelező:</span><span class="sxs-lookup"><span data-stu-id="e7faa-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="e7faa-185">Ha nem adja meg ezt a paramétert, és ez a parancsmag egy .byok fájlnévkiterjesztésű kulcsot importál, akkor a kulcsot HSM-védelem alatt lévő kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="e7faa-186">A parancsmag nem tudja importálni a kulcsot szoftver által védett kulcsként.</span><span class="sxs-lookup"><span data-stu-id="e7faa-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="e7faa-187">Ha nem adja meg ezt a paramétert, és ez a parancsmag egy .pfx fájlnévkiterjesztésű kulcsot importál, a kulcsot szoftvervédelem alatt lévő kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="e7faa-188">-Disable</span><span class="sxs-lookup"><span data-stu-id="e7faa-188">-Disable</span></span>
<span data-ttu-id="e7faa-189">Azt jelzi, hogy a hozzáadott kulcs a letiltás kezdeti állapotára van állítva.</span><span class="sxs-lookup"><span data-stu-id="e7faa-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="e7faa-190">A kulcs használatára tett minden kísérlet sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="e7faa-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="e7faa-191">Akkor használja ezt a paramétert, ha előre betölti a később engedélyezni kívánt kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="e7faa-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="e7faa-192">-Lejár</span><span class="sxs-lookup"><span data-stu-id="e7faa-192">-Expires</span></span>
<span data-ttu-id="e7faa-193">A parancsmag által adott kulcs **Lejárati** idejét adja meg DateTime-objektumként.</span><span class="sxs-lookup"><span data-stu-id="e7faa-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="e7faa-194">Ez a paraméter egyezményes világidőt (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="e7faa-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e7faa-195">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7faa-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e7faa-196">További információért írja be a `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e7faa-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="e7faa-197">Ha nem adja meg ezt a paramétert, a kulcs nem jár le.</span><span class="sxs-lookup"><span data-stu-id="e7faa-197">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="e7faa-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e7faa-198">-HsmName</span></span>
<span data-ttu-id="e7faa-199">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="e7faa-199">HSM name.</span></span> <span data-ttu-id="e7faa-200">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="e7faa-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="e7faa-201">-HsmObject</span></span>
<span data-ttu-id="e7faa-202">HSM-objektum.</span><span class="sxs-lookup"><span data-stu-id="e7faa-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="e7faa-203">-HsmResourceId</span></span>
<span data-ttu-id="e7faa-204">A HSM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e7faa-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7faa-205">-InputObject</span></span>
<span data-ttu-id="e7faa-206">Tárolóobjektum.</span><span class="sxs-lookup"><span data-stu-id="e7faa-206">Vault object.</span></span>

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

### <span data-ttu-id="e7faa-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="e7faa-207">-KeyFilePassword</span></span>
<span data-ttu-id="e7faa-208">Az importált fájl jelszavát adja meg **SecureString objektumként.**</span><span class="sxs-lookup"><span data-stu-id="e7faa-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="e7faa-209">A **SecureString objektum** beszerzéséhez használja a **ConvertTo-SecureString** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7faa-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="e7faa-210">További információért írja be a `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e7faa-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="e7faa-211">A .pfx kiterjesztésű fájlok importálásához meg kell adnia ezt a jelszót.</span><span class="sxs-lookup"><span data-stu-id="e7faa-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-212">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="e7faa-212">-KeyFilePath</span></span>
<span data-ttu-id="e7faa-213">Egy olyan helyi fájl elérési útját adja meg, amely a parancsmag által importálni kívánt legfontosabb anyagot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e7faa-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="e7faa-214">Az érvényes fájlnévkiterjesztések a .byok és a .pfx.</span><span class="sxs-lookup"><span data-stu-id="e7faa-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="e7faa-215">Ha a fájl .byok fájl, a kulcsot az importálás után automatikusan HSMs védi, és ez az alapértelmezett beállítás nem bírálható felül.</span><span class="sxs-lookup"><span data-stu-id="e7faa-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="e7faa-216">Ha a fájl .pfx fájl, a kulcsot az importálás után automatikusan szoftver védi.</span><span class="sxs-lookup"><span data-stu-id="e7faa-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="e7faa-217">Az alapértelmezett beállítás felülbírálása érdekében állítsa a Cél paramétert HSM-nek, hogy a kulcs HSM-védelem alatt ússa meg. </span><span class="sxs-lookup"><span data-stu-id="e7faa-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="e7faa-218">Ha megadja ezt a paramétert, a *Cél* paraméter megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e7faa-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="e7faa-219">-KeyOps</span></span>
<span data-ttu-id="e7faa-220">A parancsmag által hozzáadható billentyűvel elvégezhető műveletek tömbje.</span><span class="sxs-lookup"><span data-stu-id="e7faa-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="e7faa-221">Ha nem adja meg ezt a paramétert, az összes művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="e7faa-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="e7faa-222">A paraméter elfogadható értékei a [JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300)specifikációban meghatározott kulcsműveletek vesszővel elválasztott listája:</span><span class="sxs-lookup"><span data-stu-id="e7faa-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="e7faa-223">titkosítás</span><span class="sxs-lookup"><span data-stu-id="e7faa-223">encrypt</span></span>
- <span data-ttu-id="e7faa-224">visszafejtése</span><span class="sxs-lookup"><span data-stu-id="e7faa-224">decrypt</span></span>
- <span data-ttu-id="e7faa-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="e7faa-225">wrapKey</span></span>
- <span data-ttu-id="e7faa-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="e7faa-226">unwrapKey</span></span>
- <span data-ttu-id="e7faa-227">aláírás</span><span class="sxs-lookup"><span data-stu-id="e7faa-227">sign</span></span>
- <span data-ttu-id="e7faa-228">ellenőrzés</span><span class="sxs-lookup"><span data-stu-id="e7faa-228">verify</span></span>
- <span data-ttu-id="e7faa-229">importálás (csak kEK esetén lásd a 7. példát)</span><span class="sxs-lookup"><span data-stu-id="e7faa-229">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="e7faa-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e7faa-230">-KeyType</span></span>
<span data-ttu-id="e7faa-231">A kulcs kulcstípusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="e7faa-231">Specifies the key type of this key.</span></span> <span data-ttu-id="e7faa-232">BYOK-kulcsok importálása esetén az alapértelmezett érték az "RSA".</span><span class="sxs-lookup"><span data-stu-id="e7faa-232">When importing BYOK keys, it defaults to 'RSA'.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-233">-Name</span><span class="sxs-lookup"><span data-stu-id="e7faa-233">-Name</span></span>
<span data-ttu-id="e7faa-234">A kulcstárhoz hozzáadni megfelelő kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="e7faa-234">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="e7faa-235">Ez a parancsmag egy kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcstár neve és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="e7faa-235">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="e7faa-236">A névnek 1 és 63 karakter hosszúságú karakterláncnak kell lennie, amely csak 0-9, a-z, A-Z és - (kötőjelet) tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e7faa-236">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="e7faa-237">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="e7faa-237">-NotBefore</span></span>
<span data-ttu-id="e7faa-238">Azt az időt adja meg **DateTime-objektumként,** amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="e7faa-238">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="e7faa-239">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="e7faa-239">This parameter uses UTC.</span></span> <span data-ttu-id="e7faa-240">**DateTime-objektum** beszerzéséhez használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7faa-240">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e7faa-241">Ha nem adja meg ezt a paramétert, a kulcs azonnal használható.</span><span class="sxs-lookup"><span data-stu-id="e7faa-241">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="e7faa-242">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7faa-242">-ResourceId</span></span>
<span data-ttu-id="e7faa-243">Tároló erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="e7faa-243">Vault Resource Id.</span></span>

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

### <span data-ttu-id="e7faa-244">-Size</span><span class="sxs-lookup"><span data-stu-id="e7faa-244">-Size</span></span>
<span data-ttu-id="e7faa-245">RSA-billentyű mérete bitben.</span><span class="sxs-lookup"><span data-stu-id="e7faa-245">RSA key size, in bits.</span></span> <span data-ttu-id="e7faa-246">Ha nincs megadva, a szolgáltatás biztonságos alapértelmezett beállítást biztosít.</span><span class="sxs-lookup"><span data-stu-id="e7faa-246">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7faa-247">-Tag</span><span class="sxs-lookup"><span data-stu-id="e7faa-247">-Tag</span></span>
<span data-ttu-id="e7faa-248">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="e7faa-248">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7faa-249">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="e7faa-249">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e7faa-250">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e7faa-250">-VaultName</span></span>
<span data-ttu-id="e7faa-251">Annak a kulcstárnak a nevét adja meg, amelyhez ez a parancsmag hozzáadja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="e7faa-251">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="e7faa-252">Ez a parancsmag egy kulcstár FQDN-ét építi fel a paraméter által megadott név és az aktuális környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="e7faa-252">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="e7faa-253">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7faa-253">-Confirm</span></span>
<span data-ttu-id="e7faa-254">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7faa-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7faa-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7faa-255">-WhatIf</span></span>
<span data-ttu-id="e7faa-256">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7faa-256">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7faa-257">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7faa-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7faa-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7faa-258">CommonParameters</span></span>
<span data-ttu-id="e7faa-259">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7faa-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7faa-260">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7faa-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7faa-261">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7faa-261">INPUTS</span></span>

### <span data-ttu-id="e7faa-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e7faa-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e7faa-263">System.String</span><span class="sxs-lookup"><span data-stu-id="e7faa-263">System.String</span></span>

## <span data-ttu-id="e7faa-264">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7faa-264">OUTPUTS</span></span>

### <span data-ttu-id="e7faa-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7faa-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="e7faa-266">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7faa-266">NOTES</span></span>

## <span data-ttu-id="e7faa-267">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7faa-267">RELATED LINKS</span></span>

[<span data-ttu-id="e7faa-268">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7faa-268">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="e7faa-269">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7faa-269">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="e7faa-270">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7faa-270">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

