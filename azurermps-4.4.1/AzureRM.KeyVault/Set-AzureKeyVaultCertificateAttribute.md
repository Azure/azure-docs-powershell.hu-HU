---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://go.microsoft.com/fwlink/?LinkId=822861
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: b8dac56d55446915af1c9a2f00f71d903f3daf03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505931"
---
# <span data-ttu-id="7cbe6-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="7cbe6-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="7cbe6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7cbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbe6-103">Módosítja a tanúsítványok szerkeszthető attribútumait.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cbe6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7cbe6-104">SYNTAX</span></span>

```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cbe6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7cbe6-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbe6-106">A **set-AzureKeyVaultCertificateAttribute** parancsmag a tanúsítványok szerkeszthető attribútumait módosítja.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-106">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="7cbe6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7cbe6-107">EXAMPLES</span></span>

### <span data-ttu-id="7cbe6-108">Példa 1: a tanúsítvánnyal társított címkék módosítása</span><span class="sxs-lookup"><span data-stu-id="7cbe6-108">Example 1: Modify the tags associated with a certificate</span></span>
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

<span data-ttu-id="7cbe6-109">Az első parancs kulcs/érték párok tömbjét rendeli hozzá a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="7cbe6-110">A második parancs beállítja a TestCert01 nevű tanúsítvány címkék értékét $Tags.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="7cbe6-111">A végleges parancs a TestCert01 tanúsítványát az Get-AzureKeyVaultCertificate parancsmag használatával jeleníti meg a művelet ellenőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-111">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="7cbe6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7cbe6-112">PARAMETERS</span></span>

### <span data-ttu-id="7cbe6-113">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="7cbe6-113">-Enable</span></span>
<span data-ttu-id="7cbe6-114">Azt jelzi, hogy be van-e jelölve a tanúsítványok engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-114">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="7cbe6-115">Adja meg, hogy a $True engedélyezze vagy $False a letiltást.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-115">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7cbe6-116">-Name</span></span>
<span data-ttu-id="7cbe6-117">A módosítani kívánt tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-117">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="7cbe6-118">Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-118">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cbe6-119">-PassThru</span></span>
<span data-ttu-id="7cbe6-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7cbe6-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7cbe6-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="7cbe6-122">-Tag</span></span>
<span data-ttu-id="7cbe6-123">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7cbe6-124">Példa:</span><span class="sxs-lookup"><span data-stu-id="7cbe6-124">For example:</span></span>

<span data-ttu-id="7cbe6-125">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="7cbe6-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe6-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7cbe6-126">-VaultName</span></span>
<span data-ttu-id="7cbe6-127">Annak a kulcsnak a neve, amelyben ez a parancsmag módosította a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-127">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="7cbe6-128">Ez a parancsmag a kulcsfájl teljes tartománynevét építi ki a név és a jelenleg kijelölt környezet alapján.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-128">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe6-129">-Verzió</span><span class="sxs-lookup"><span data-stu-id="7cbe6-129">-Version</span></span>
<span data-ttu-id="7cbe6-130">A tanúsítvány verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-130">Specifies the version of a certificate.</span></span>
<span data-ttu-id="7cbe6-131">Ez a parancsmag a tanúsítványok teljes tartománynevét, az aktuálisan kijelölt környezetet, a tanúsítvány nevét és a tanúsítvány verziószámát építi fel.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-131">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe6-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7cbe6-132">-Confirm</span></span>
<span data-ttu-id="7cbe6-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbe6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbe6-134">-WhatIf</span></span>
<span data-ttu-id="7cbe6-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbe6-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbe6-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbe6-137">-DefaultProfile</span></span>
<span data-ttu-id="7cbe6-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbe6-139">CommonParameters</span></span>
<span data-ttu-id="7cbe6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7cbe6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbe6-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbe6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cbe6-142">INPUTS</span></span>

## <span data-ttu-id="7cbe6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cbe6-143">OUTPUTS</span></span>

### <span data-ttu-id="7cbe6-144">Microsoft. Azure. Command. KeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="7cbe6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7cbe6-145">NOTES</span></span>

## <span data-ttu-id="7cbe6-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cbe6-146">RELATED LINKS</span></span>

[<span data-ttu-id="7cbe6-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7cbe6-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
