---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7955ecd02d40ac3dff891b8eb315a39ccf985ebb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680362"
---
# <span data-ttu-id="400a3-101">Restore-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="400a3-101">Restore-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="400a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="400a3-102">SYNOPSIS</span></span>
<span data-ttu-id="400a3-103">Egy biztonsági másolatból visszaállítja a tanúsítványt a biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="400a3-103">Restores a certificate in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="400a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="400a3-104">SYNTAX</span></span>

### <span data-ttu-id="400a3-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="400a3-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="400a3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="400a3-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="400a3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="400a3-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="400a3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="400a3-108">DESCRIPTION</span></span>
<span data-ttu-id="400a3-109">A **Restore-AzureKeyVaultCertificate** parancsmag egy biztonsági másolatból hoz létre egy tanúsítványt a megadott kulcs-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="400a3-109">The **Restore-AzureKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="400a3-110">Ez a tanúsítvány a bemeneti fájlban a mentett tanúsítvány másolata, és az eredeti tanúsítvánnyal megegyező név.</span><span class="sxs-lookup"><span data-stu-id="400a3-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="400a3-111">Ha a kulcsfájl már tartalmaz tanúsítványokat ugyanazzal a névvel, az eredeti tanúsítvány felülírása helyett ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="400a3-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="400a3-112">Ha a biztonsági másolat több verziót tartalmaz, a rendszer visszaállítja az összes verziót.</span><span class="sxs-lookup"><span data-stu-id="400a3-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="400a3-113">Annak a kulcsnak a boltozata, amelynek a tanúsítványát vissza szeretné állítani, eltérhetnek attól a fő tárolótól, amelyről biztonsági másolatot készített a tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="400a3-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="400a3-114">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="400a3-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="400a3-115">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="400a3-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="400a3-116">Példák</span><span class="sxs-lookup"><span data-stu-id="400a3-116">EXAMPLES</span></span>

### <span data-ttu-id="400a3-117">1. példa: biztonsági másolatot tartalmazó tanúsítvány visszaállítása</span><span class="sxs-lookup"><span data-stu-id="400a3-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="400a3-118">Ez a parancs visszaállítja a tanúsítványt, az összes verzióját is, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatba.</span><span class="sxs-lookup"><span data-stu-id="400a3-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="400a3-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="400a3-119">PARAMETERS</span></span>

### <span data-ttu-id="400a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="400a3-120">-DefaultProfile</span></span>
<span data-ttu-id="400a3-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="400a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="400a3-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="400a3-122">-InputFile</span></span>
<span data-ttu-id="400a3-123">Bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="400a3-123">Input file.</span></span>
<span data-ttu-id="400a3-124">A mentett blobot tartalmazó bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="400a3-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400a3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="400a3-125">-InputObject</span></span>
<span data-ttu-id="400a3-126">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="400a3-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="400a3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="400a3-127">-ResourceId</span></span>
<span data-ttu-id="400a3-128">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="400a3-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="400a3-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="400a3-129">-VaultName</span></span>
<span data-ttu-id="400a3-130">Boltozat neve.</span><span class="sxs-lookup"><span data-stu-id="400a3-130">Vault name.</span></span>
<span data-ttu-id="400a3-131">A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="400a3-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400a3-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="400a3-132">-Confirm</span></span>
<span data-ttu-id="400a3-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="400a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="400a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="400a3-134">-WhatIf</span></span>
<span data-ttu-id="400a3-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="400a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="400a3-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="400a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="400a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="400a3-137">CommonParameters</span></span>
<span data-ttu-id="400a3-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="400a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="400a3-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="400a3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="400a3-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="400a3-140">INPUTS</span></span>

### <span data-ttu-id="400a3-141">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="400a3-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="400a3-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="400a3-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="400a3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="400a3-143">System.String</span></span>

## <span data-ttu-id="400a3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="400a3-144">OUTPUTS</span></span>

### <span data-ttu-id="400a3-145">Microsoft. Azure. Command. PSKeyVaultCertificate. models.</span><span class="sxs-lookup"><span data-stu-id="400a3-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="400a3-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="400a3-146">NOTES</span></span>

## <span data-ttu-id="400a3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="400a3-147">RELATED LINKS</span></span>
