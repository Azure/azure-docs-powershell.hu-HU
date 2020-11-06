---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: 4aac9e7079451eebda0c77ae663666fbd55dc9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492263"
---
# <span data-ttu-id="a71c9-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="a71c9-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="a71c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a71c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a71c9-103">Módosítja a tanúsítványok szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="a71c9-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a71c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a71c9-104">SYNTAX</span></span>

### <span data-ttu-id="a71c9-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a71c9-105">ByName (Default)</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a71c9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a71c9-106">ByInputObject</span></span>
```
Set-AzureKeyVaultCertificateAttribute [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71c9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a71c9-107">DESCRIPTION</span></span>
<span data-ttu-id="a71c9-108">A **set-AzureKeyVaultCertificateAttribute** parancsmag a tanúsítványok szerkeszthető attribútumait módosítja.</span><span class="sxs-lookup"><span data-stu-id="a71c9-108">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="a71c9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a71c9-109">EXAMPLES</span></span>

### <span data-ttu-id="a71c9-110">Példa 1: a tanúsítvánnyal társított címkék módosítása</span><span class="sxs-lookup"><span data-stu-id="a71c9-110">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="a71c9-111">Az első parancs kulcs/érték párok tömbjét rendeli hozzá a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="a71c9-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="a71c9-112">A második parancs beállítja a TestCert01 nevű tanúsítvány címkék értékét $Tags.</span><span class="sxs-lookup"><span data-stu-id="a71c9-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="a71c9-113">A végleges parancs a TestCert01 tanúsítványát az Get-AzureKeyVaultCertificate parancsmag használatával jeleníti meg a művelet ellenőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="a71c9-113">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="a71c9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a71c9-114">PARAMETERS</span></span>

### <span data-ttu-id="a71c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71c9-115">-DefaultProfile</span></span>
<span data-ttu-id="a71c9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a71c9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71c9-117">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="a71c9-117">-Enable</span></span>
<span data-ttu-id="a71c9-118">Azt jelzi, hogy be van-e jelölve a tanúsítványok engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="a71c9-118">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="a71c9-119">Adja meg, hogy a $True engedélyezze vagy $False a letiltást.</span><span class="sxs-lookup"><span data-stu-id="a71c9-119">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a71c9-120">-InputObject</span></span>
<span data-ttu-id="a71c9-121">Certificate objektum</span><span class="sxs-lookup"><span data-stu-id="a71c9-121">Certificate object</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a71c9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a71c9-122">-Name</span></span>
<span data-ttu-id="a71c9-123">A módosítani kívánt tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a71c9-123">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="a71c9-124">Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="a71c9-124">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a71c9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a71c9-125">-PassThru</span></span>
<span data-ttu-id="a71c9-126">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a71c9-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a71c9-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a71c9-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a71c9-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="a71c9-128">-Tag</span></span>
<span data-ttu-id="a71c9-129">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="a71c9-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a71c9-130">Példa:</span><span class="sxs-lookup"><span data-stu-id="a71c9-130">For example:</span></span>

<span data-ttu-id="a71c9-131">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="a71c9-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a71c9-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a71c9-132">-VaultName</span></span>
<span data-ttu-id="a71c9-133">Annak a kulcsnak a neve, amelyben ez a parancsmag módosította a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="a71c9-133">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="a71c9-134">Ez a parancsmag a kulcsfájl teljes tartománynevét építi ki a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="a71c9-134">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a71c9-135">-Verzió</span><span class="sxs-lookup"><span data-stu-id="a71c9-135">-Version</span></span>
<span data-ttu-id="a71c9-136">A tanúsítvány verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a71c9-136">Specifies the version of a certificate.</span></span>
<span data-ttu-id="a71c9-137">Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="a71c9-137">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a71c9-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a71c9-138">-Confirm</span></span>
<span data-ttu-id="a71c9-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a71c9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a71c9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71c9-140">-WhatIf</span></span>
<span data-ttu-id="a71c9-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a71c9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a71c9-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a71c9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a71c9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71c9-143">CommonParameters</span></span>
<span data-ttu-id="a71c9-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a71c9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71c9-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a71c9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71c9-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a71c9-146">INPUTS</span></span>

### <span data-ttu-id="a71c9-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="a71c9-147">None</span></span>
<span data-ttu-id="a71c9-148">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a71c9-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a71c9-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a71c9-149">OUTPUTS</span></span>

### <span data-ttu-id="a71c9-150">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="a71c9-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="a71c9-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a71c9-151">NOTES</span></span>

## <span data-ttu-id="a71c9-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a71c9-152">RELATED LINKS</span></span>

[<span data-ttu-id="a71c9-153">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a71c9-153">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
