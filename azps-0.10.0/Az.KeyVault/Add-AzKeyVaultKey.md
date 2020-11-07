---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843910"
---
# <span data-ttu-id="11078-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11078-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="11078-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11078-102">SYNOPSIS</span></span>
<span data-ttu-id="11078-103">Billentyűt hoz létre a fő tárolóban, vagy egy kulcsot egy fő boltozatba importál.</span><span class="sxs-lookup"><span data-stu-id="11078-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="11078-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11078-104">SYNTAX</span></span>

### <span data-ttu-id="11078-105">Létrehozás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11078-105">Create (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11078-106">Importálása</span><span class="sxs-lookup"><span data-stu-id="11078-106">Import</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11078-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="11078-107">DESCRIPTION</span></span>
<span data-ttu-id="11078-108">Az **Add-AzKeyVaultKey** parancsmag egy billentyűt hoz létre az Azure Key Vault-ban, vagy egy kulcsot importál egy fő boltozatba.</span><span class="sxs-lookup"><span data-stu-id="11078-108">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="11078-109">Ezzel a parancsmaggal a következő módszerekkel adhat hozzá kulcsokat:</span><span class="sxs-lookup"><span data-stu-id="11078-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="11078-110">Hozzon létre egy kulcsot egy hardveres biztonsági modulban (HSM) a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="11078-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="11078-111">Kulcsot hozhat létre a szoftverben a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="11078-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="11078-112">Importáljon egy kulcsot a saját hardver biztonsági modulból (HSM) a HSM a Key Vault szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="11078-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="11078-113">Importáljon egy kulcsot egy. pfx fájlból a számítógépre.</span><span class="sxs-lookup"><span data-stu-id="11078-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="11078-114">Importáljon egy kulcsot egy. pfx fájlból a számítógépen a hardver biztonsági moduljaihoz (HSM) a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="11078-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="11078-115">A fenti műveletek bármelyikével alapvető attribútumokat adhat meg, illetve elfogadhat alapértelmezett beállításokat.</span><span class="sxs-lookup"><span data-stu-id="11078-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="11078-116">Ha olyan billentyűt hoz létre vagy importál, amelynek a neve megegyezik egy meglévő kulccsal, az eredeti kulcs frissül az új kulcshoz megadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="11078-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="11078-117">A korábbi értékeket a kulcs adott verziójához tartozó, a verziószámot tartalmazó URI-azonosító használatával érheti el.</span><span class="sxs-lookup"><span data-stu-id="11078-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="11078-118">A főbb verziókkal és az URI-struktúrájával kapcsolatos tudnivalók a [kulcsok andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) a Key Vault REST API-ban című dokumentumban olvashatók.</span><span class="sxs-lookup"><span data-stu-id="11078-118">To learn about key versions and the URI structure, see [About Keys andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="11078-119">Megjegyzés: Ha egy kulcsot saját hardveres biztonsági modulból szeretne importálni, először létre kell hoznia egy BYOK-csomagot (. BYOK fájlnév-kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészlet használatával.</span><span class="sxs-lookup"><span data-stu-id="11078-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="11078-120">További információt a [HSM-Protected kulcsok létrehozása és továbbítása az Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252)-ban című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="11078-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="11078-121">Ajánlott eljárásként készítsen biztonsági másolatot a kulcsról, miután létrehozta vagy frissíti őket a Backup-AzKeyVaultKey parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="11078-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="11078-122">Nincs eltávolítási funkció, ezért ha véletlenül törli a billentyűt vagy törli, majd meggondolja magát, a kulcs nem állítható helyre, hacsak nem rendelkezik biztonsági másolattal.</span><span class="sxs-lookup"><span data-stu-id="11078-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="11078-123">Példák</span><span class="sxs-lookup"><span data-stu-id="11078-123">EXAMPLES</span></span>

### <span data-ttu-id="11078-124">Példa 1: kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="11078-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="11078-125">Ez a parancs létrehoz egy ITSoftware nevű, a contoso nevű kulcsfájl nevű kulccsal védett kulcsot.</span><span class="sxs-lookup"><span data-stu-id="11078-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="11078-126">2. példa: HSM-védelemmel ellátott kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="11078-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="11078-127">Ez a parancs egy HSM-védelemmel ellátott billentyűt hoz létre a contoso nevű kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="11078-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="11078-128">3. példa: kulcs létrehozása nem alapértelmezett értékekkel</span><span class="sxs-lookup"><span data-stu-id="11078-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="11078-129">Az első parancs a $KeyOperations változóban tárolja az értékeket dekódolja és ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="11078-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="11078-130">A második parancs létrehoz egy **datetime** típusú objektumot, amelyet az UTC a **Get-Date** parancsmag használatával definiál.</span><span class="sxs-lookup"><span data-stu-id="11078-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="11078-131">Ez az objektum két év múlva adja meg a jövőbeli időpontot.</span><span class="sxs-lookup"><span data-stu-id="11078-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="11078-132">A parancs a $Expires változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="11078-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="11078-133">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="11078-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="11078-134">A harmadik parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="11078-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="11078-135">Az objektum a jelenlegi UTC időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="11078-135">That object specifies current UTC time.</span></span> <span data-ttu-id="11078-136">A parancs a $NotBefore változóban tárolja a dátumot.</span><span class="sxs-lookup"><span data-stu-id="11078-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="11078-137">A végleges parancs létrehoz egy ITHsmNonDefault, amely egy HSM-védelemmel ellátott kulcs.</span><span class="sxs-lookup"><span data-stu-id="11078-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="11078-138">A parancs a $KeyOperations tárolt, engedélyezett műveletek értékeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="11078-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="11078-139">A parancs az előző parancsokban létrehozott *lejáratok* és *NotBefore* paramétereinek időpontját adja meg, valamint a nagy SÚLYOSSÁGú és az IT-címkéket.</span><span class="sxs-lookup"><span data-stu-id="11078-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="11078-140">Az új kulcs le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="11078-140">The new key is disabled.</span></span> <span data-ttu-id="11078-141">A **set-AzKeyVaultKey** parancsmag használatával engedélyezheti azt.</span><span class="sxs-lookup"><span data-stu-id="11078-141">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="11078-142">Példa 4: HSM-védelemmel ellátott kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="11078-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="11078-143">Ez a parancs a ITByok nevű kulcsot a *KeyFilePath* paraméter által megadott helyről importálja.</span><span class="sxs-lookup"><span data-stu-id="11078-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="11078-144">Az importált kulcs egy HSM-védelemmel ellátott kulcs.</span><span class="sxs-lookup"><span data-stu-id="11078-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="11078-145">Ha egy kulcsot saját hardveres biztonsági modulból szeretne importálni, először létre kell hoznia egy BYOK-csomagot (. BYOK fájlnév-kiterjesztésű fájlt) az Azure Key Vault BYOK eszközkészlet használatával.</span><span class="sxs-lookup"><span data-stu-id="11078-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="11078-146">További információt a [HSM-Protected kulcsok létrehozása és továbbítása az Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252)-ban című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="11078-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="11078-147">Példa 5: szoftverrel védett kulcs importálása</span><span class="sxs-lookup"><span data-stu-id="11078-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="11078-148">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="11078-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="11078-149">További információért írja be a következőt: `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="11078-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="11078-150">A második parancs a contoso Key Vault-ban hozza létre a szoftverhez tartozó jelszót.</span><span class="sxs-lookup"><span data-stu-id="11078-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="11078-151">A parancs a $Passwordban tárolt kulcs és jelszó helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11078-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="11078-152">6. példa: kulcs importálása és attribútumok hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="11078-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="11078-153">Az első parancs a karakterláncot egy biztonságos karakterláncba a **ConvertTo-SecureString** parancsmag használatával konvertálja, majd a karakterláncot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="11078-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="11078-154">A második parancs egy **datetime** típusú objektumot hoz létre a **Get-Date** parancsmag használatával, majd az objektumot az $Expires változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="11078-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="11078-155">A harmadik parancs a $tags változót hozza létre a nagy súlyosságú és a címkék beállításához.</span><span class="sxs-lookup"><span data-stu-id="11078-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="11078-156">A végleges parancs a megadott helyről importálja a kulcsot a HSM-kulcsként.</span><span class="sxs-lookup"><span data-stu-id="11078-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="11078-157">A parancs a $Password tárolt $Expires és jelszóban tárolt elévülési időt adja meg, és a $tagsban tárolt címkéket alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="11078-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="11078-158">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11078-158">PARAMETERS</span></span>

### <span data-ttu-id="11078-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11078-159">-DefaultProfile</span></span>
<span data-ttu-id="11078-160">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11078-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11078-161">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="11078-161">-Destination</span></span>
<span data-ttu-id="11078-162">Itt adhatja meg, hogy a kulcsot szoftverrel védett kulcsként vagy HSM-védelemmel ellátott kulccsal szeretné-e hozzáadni a Key Vault szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="11078-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="11078-163">Érvényes értékek: HSM és szoftver.</span><span class="sxs-lookup"><span data-stu-id="11078-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="11078-164">Megjegyzés: Ha a HSM-t célként szeretné használni, rendelkeznie kell a HSM támogató fő tárolóval.</span><span class="sxs-lookup"><span data-stu-id="11078-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="11078-165">Az Azure Key Vault szolgáltatás szintjeiről és képességeiről további információt az [Azure Key Vault árképzési webhelyén](http://go.microsoft.com/fwlink/?linkid=512521)találhat.</span><span class="sxs-lookup"><span data-stu-id="11078-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="11078-166">Ezt a paramétert új kulcs létrehozásakor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="11078-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="11078-167">Ha a *KeyFilePath* paraméterrel importál egy billentyűt, akkor ez a paraméter nem kötelező:</span><span class="sxs-lookup"><span data-stu-id="11078-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="11078-168">Ha nem adja meg ezt a paramétert, és ez a parancsmag olyan kulcsot importál, amely. byok fájlnév-kiterjesztéssel rendelkezik, a kulcsot HSM-védelemmel ellátott kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="11078-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="11078-169">A parancsmag nem tudja importálni a kulcsot szoftveres védelemmel ellátott kulcsként.</span><span class="sxs-lookup"><span data-stu-id="11078-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="11078-170">Ha nem adja meg ezt a paramétert, és ez a parancsmag a. pfx fájlnév-kiterjesztésű kulcsot importálja, az a kulcsot szoftveres védelemmel ellátott kulcsként importálja.</span><span class="sxs-lookup"><span data-stu-id="11078-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11078-171">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="11078-171">-Disable</span></span>
<span data-ttu-id="11078-172">Azt jelzi, hogy a felvenni kívánt kulcs a letiltott állapotú eredeti állapotra van állítva.</span><span class="sxs-lookup"><span data-stu-id="11078-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="11078-173">A billentyű használatát minden próbálkozás sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="11078-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="11078-174">Akkor használja ezt a paramétert, ha előre betöltődik a később engedélyezni kívánt billentyűk.</span><span class="sxs-lookup"><span data-stu-id="11078-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="11078-175">-Lejár</span><span class="sxs-lookup"><span data-stu-id="11078-175">-Expires</span></span>
<span data-ttu-id="11078-176">A lejárati idő **datetime** objektumként való megadása a parancsmag által hozzáadott kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="11078-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="11078-177">Ez a paraméter koordinált univerzális időpontot (UTC) használ.</span><span class="sxs-lookup"><span data-stu-id="11078-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="11078-178">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11078-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="11078-179">További információért írja be a következőt: `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="11078-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="11078-180">Ha nem adja meg ezt a paramétert, a kulcs nem jár le.</span><span class="sxs-lookup"><span data-stu-id="11078-180">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11078-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="11078-181">-KeyFilePassword</span></span>
<span data-ttu-id="11078-182">Az importált fájlhoz tartozó jelszót **SecureString** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="11078-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="11078-183">**SecureString** objektum beolvasásához használja a **ConvertTo-SecureString** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11078-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="11078-184">További információért írja be a következőt: `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="11078-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="11078-185">A. pfx fájlnév-kiterjesztésű fájlok importálásához meg kell adnia ezt a jelszót.</span><span class="sxs-lookup"><span data-stu-id="11078-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11078-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="11078-186">-KeyFilePath</span></span>
<span data-ttu-id="11078-187">A parancsmag által importált fontos anyagot tartalmazó helyi fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="11078-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="11078-188">Az érvényes fájlnév-kiterjesztések. byok és. pfx.</span><span class="sxs-lookup"><span data-stu-id="11078-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="11078-189">Ha a fájl. byok fájl, az importálás után a rendszer automatikusan védi a kulcsot, és nem tudja felülírni ezt az alapértelmezett HSM.</span><span class="sxs-lookup"><span data-stu-id="11078-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="11078-190">Ha a fájl. pfx fájl, a kulcs automatikusan védett a szoftverrel az importálás után.</span><span class="sxs-lookup"><span data-stu-id="11078-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="11078-191">Az alapértelmezett beállítás felülbírálásához állítsa a *cél* paramétert a HSM értékre, hogy a kulcs HSM-védelemmel legyen ellátva.</span><span class="sxs-lookup"><span data-stu-id="11078-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="11078-192">Ha ezt a paramétert adja meg, a *cél* paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="11078-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11078-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="11078-193">-KeyOps</span></span>
<span data-ttu-id="11078-194">Megadja azokat a műveleteket, amelyeket a parancsmag által hozzáadott kulccsal végezhet el.</span><span class="sxs-lookup"><span data-stu-id="11078-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="11078-195">Ha nem adja meg ezt a paramétert, akkor az összes művelet elvégezhető.</span><span class="sxs-lookup"><span data-stu-id="11078-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="11078-196">A paraméter elfogadható értékei: a [JSON-webkulcs (JWK) specifikációja](http://go.microsoft.com/fwlink/?LinkID=613300)által meghatározott főbb műveletek vesszővel elválasztott listája:</span><span class="sxs-lookup"><span data-stu-id="11078-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="11078-197">Beavatkozik</span><span class="sxs-lookup"><span data-stu-id="11078-197">Encrypt</span></span>
- <span data-ttu-id="11078-198">Visszafejtése</span><span class="sxs-lookup"><span data-stu-id="11078-198">Decrypt</span></span>
- <span data-ttu-id="11078-199">Wrap</span><span class="sxs-lookup"><span data-stu-id="11078-199">Wrap</span></span>
- <span data-ttu-id="11078-200">Tördelésének megszüntetéséhez</span><span class="sxs-lookup"><span data-stu-id="11078-200">Unwrap</span></span>
- <span data-ttu-id="11078-201">Jel</span><span class="sxs-lookup"><span data-stu-id="11078-201">Sign</span></span>
- <span data-ttu-id="11078-202">Ellenőrizze</span><span class="sxs-lookup"><span data-stu-id="11078-202">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11078-203">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11078-203">-Name</span></span>
<span data-ttu-id="11078-204">Annak a kulcsnak a nevét adja meg, amelyet fel szeretne venni a kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="11078-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="11078-205">Ez a parancsmag a kulcs teljes tartománynevét (FQDN) építi fel a paraméter által megadott név, a kulcsfájl neve és a jelenlegi környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="11078-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="11078-206">A névnek 0-9 csak az 1-es, a-z, A-z és A-(a kötőjel szimbólumot) tartalmazó 63-karakterből kell állnia.</span><span class="sxs-lookup"><span data-stu-id="11078-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11078-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="11078-207">-NotBefore</span></span>
<span data-ttu-id="11078-208">Itt adhatja meg az időt **datetime** objektumként, amely előtt a kulcs nem használható.</span><span class="sxs-lookup"><span data-stu-id="11078-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="11078-209">Ez a paraméter az UTC-t használja.</span><span class="sxs-lookup"><span data-stu-id="11078-209">This parameter uses UTC.</span></span> <span data-ttu-id="11078-210">Ha egy **datetime** típusú objektumot szeretne beolvasni, használja a **Get-Date** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11078-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="11078-211">Ha nem adja meg ezt a paramétert, akkor a billentyű azonnal használható.</span><span class="sxs-lookup"><span data-stu-id="11078-211">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11078-212">-Címke</span><span class="sxs-lookup"><span data-stu-id="11078-212">-Tag</span></span>
<span data-ttu-id="11078-213">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="11078-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="11078-214">Példa:</span><span class="sxs-lookup"><span data-stu-id="11078-214">For example:</span></span>

<span data-ttu-id="11078-215">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="11078-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11078-216">-VaultName</span><span class="sxs-lookup"><span data-stu-id="11078-216">-VaultName</span></span>
<span data-ttu-id="11078-217">Annak a kulcsnak a nevét adja meg, amelyre a parancsmag hozzáadja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="11078-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="11078-218">Ez a parancsmag a kulcsfájl teljes tartománynevét a paraméter által megadott név és a jelenlegi környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="11078-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="11078-219">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11078-219">-Confirm</span></span>
<span data-ttu-id="11078-220">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11078-220">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11078-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11078-221">-WhatIf</span></span>
<span data-ttu-id="11078-222">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11078-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11078-223">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11078-223">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11078-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11078-224">CommonParameters</span></span>
<span data-ttu-id="11078-225">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11078-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11078-226">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11078-226">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11078-227">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11078-227">INPUTS</span></span>

### <span data-ttu-id="11078-228">Nincs</span><span class="sxs-lookup"><span data-stu-id="11078-228">None</span></span>
<span data-ttu-id="11078-229">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="11078-229">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11078-230">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11078-230">OUTPUTS</span></span>

### <span data-ttu-id="11078-231">Microsoft. Azure. Command. Vault. models. Bundle</span><span class="sxs-lookup"><span data-stu-id="11078-231">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="11078-232">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11078-232">NOTES</span></span>

## <span data-ttu-id="11078-233">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11078-233">RELATED LINKS</span></span>

[<span data-ttu-id="11078-234">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11078-234">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="11078-235">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11078-235">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="11078-236">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11078-236">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="11078-237">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="11078-237">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
