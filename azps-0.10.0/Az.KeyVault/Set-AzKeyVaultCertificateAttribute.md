---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
ms.openlocfilehash: 9297e523e623542c19df1915d3da29d9e39cec40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843857"
---
# <span data-ttu-id="3f5c9-101">Set-AzKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="3f5c9-101">Set-AzKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="3f5c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5c9-103">Módosítja a tanúsítványok szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="3f5c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f5c9-104">SYNTAX</span></span>

```
Set-AzKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f5c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="3f5c9-106">A **set-AzKeyVaultCertificateAttribute** parancsmag a tanúsítványok szerkeszthető attribútumait módosítja.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-106">The **Set-AzKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="3f5c9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3f5c9-107">EXAMPLES</span></span>

### <span data-ttu-id="3f5c9-108">Példa 1: a tanúsítvánnyal társított címkék módosítása</span><span class="sxs-lookup"><span data-stu-id="3f5c9-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="3f5c9-109">Az első parancs kulcs/érték párok tömbjét rendeli hozzá a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="3f5c9-110">A második parancs beállítja a TestCert01 nevű tanúsítvány címkék értékét $Tags.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="3f5c9-111">A végleges parancs a TestCert01 tanúsítványát az Get-AzKeyVaultCertificate parancsmag használatával jeleníti meg a művelet ellenőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-111">The final command displays the TestCert01 certificate by using the Get-AzKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="3f5c9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f5c9-112">PARAMETERS</span></span>

### <span data-ttu-id="3f5c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5c9-113">-DefaultProfile</span></span>
<span data-ttu-id="3f5c9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3f5c9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f5c9-115">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="3f5c9-115">-Enable</span></span>
<span data-ttu-id="3f5c9-116">Azt jelzi, hogy be van-e jelölve a tanúsítványok engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="3f5c9-117">Adja meg, hogy a $True engedélyezze vagy $False a letiltást.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-117">Specify $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="3f5c9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f5c9-118">-Name</span></span>
<span data-ttu-id="3f5c9-119">A módosítani kívánt tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="3f5c9-120">Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5c9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f5c9-121">-PassThru</span></span>
<span data-ttu-id="3f5c9-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f5c9-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f5c9-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="3f5c9-124">-Tag</span></span>
<span data-ttu-id="3f5c9-125">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3f5c9-126">Példa:</span><span class="sxs-lookup"><span data-stu-id="3f5c9-126">For example:</span></span>

<span data-ttu-id="3f5c9-127">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3f5c9-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3f5c9-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3f5c9-128">-VaultName</span></span>
<span data-ttu-id="3f5c9-129">Annak a kulcsnak a neve, amelyben ez a parancsmag módosította a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="3f5c9-130">Ez a parancsmag a kulcsfájl teljes tartománynevét építi ki a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3f5c9-131">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3f5c9-131">-Version</span></span>
<span data-ttu-id="3f5c9-132">A tanúsítvány verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="3f5c9-133">Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

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

### <span data-ttu-id="3f5c9-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f5c9-134">-Confirm</span></span>
<span data-ttu-id="3f5c9-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f5c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f5c9-136">-WhatIf</span></span>
<span data-ttu-id="3f5c9-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f5c9-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f5c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5c9-139">CommonParameters</span></span>
<span data-ttu-id="3f5c9-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f5c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5c9-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f5c9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5c9-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f5c9-142">INPUTS</span></span>

### <span data-ttu-id="3f5c9-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="3f5c9-143">None</span></span>
<span data-ttu-id="3f5c9-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f5c9-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f5c9-145">OUTPUTS</span></span>

### <span data-ttu-id="3f5c9-146">Microsoft. Azure. Command. KeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="3f5c9-146">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="3f5c9-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f5c9-147">NOTES</span></span>

## <span data-ttu-id="3f5c9-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f5c9-148">RELATED LINKS</span></span>

[<span data-ttu-id="3f5c9-149">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3f5c9-149">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)
