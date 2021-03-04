---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 4af261f10a4d5f3d7228f31b511a092600cb93bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918857"
---
# <span data-ttu-id="ad99d-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ad99d-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="ad99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad99d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad99d-103">Visszaállít egy tanúsítványt egy biztonsági másolatból egy kulcstárolóban.</span><span class="sxs-lookup"><span data-stu-id="ad99d-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="ad99d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad99d-104">SYNTAX</span></span>

### <span data-ttu-id="ad99d-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad99d-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad99d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad99d-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad99d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad99d-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad99d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad99d-108">DESCRIPTION</span></span>
<span data-ttu-id="ad99d-109">A **Restore-AzKeyVaultCertificate** parancsmag egy biztonsági másolatból létrehoz egy tanúsítványt a megadott kulcstárolóban.</span><span class="sxs-lookup"><span data-stu-id="ad99d-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="ad99d-110">Ez a tanúsítvány a bemeneti fájlban található biztonsági másolat másolata, és a neve megegyezik az eredeti tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="ad99d-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="ad99d-111">Ha a kulcstároló már tartalmaz egy azonos nevű tanúsítványt, a parancsmag nem tudja felülírni az eredeti tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="ad99d-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="ad99d-112">Ha a biztonsági másolat egy tanúsítvány több verzióját tartalmazza, a rendszer az összes verziót visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="ad99d-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="ad99d-113">A kulcstároló, amelybe visszaállítja a tanúsítványt, eltérhet attól a kulcstárolótól, amelyről a tanúsítványt biztonsági másolatban tárolta.</span><span class="sxs-lookup"><span data-stu-id="ad99d-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="ad99d-114">A kulcstárnak azonban ugyanazt az előfizetést kell használnia, és ugyanabban a földrajzi régióban (például Észak-Amerikában) kell lennie egy Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="ad99d-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ad99d-115">Az Azure-régiók földrajzokkal való megfeleltetését a Microsoft Azure Trust Center https://azure.microsoft.com/support/trust-center/) webhelyén tudja meg.</span><span class="sxs-lookup"><span data-stu-id="ad99d-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ad99d-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad99d-116">EXAMPLES</span></span>

### <span data-ttu-id="ad99d-117">1. példa: Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ad99d-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="ad99d-118">Ez a parancs visszaállít egy tanúsítványt az összes verziójával együtt a Backup.blob nevű biztonságimásolat-fájlból a MyKeyVault nevű kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="ad99d-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ad99d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad99d-119">PARAMETERS</span></span>

### <span data-ttu-id="ad99d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad99d-120">-DefaultProfile</span></span>
<span data-ttu-id="ad99d-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad99d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad99d-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ad99d-122">-InputFile</span></span>
<span data-ttu-id="ad99d-123">Bemeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="ad99d-123">Input file.</span></span>
<span data-ttu-id="ad99d-124">A háttérként tárolt blobot tartalmazó bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="ad99d-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="ad99d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad99d-125">-InputObject</span></span>
<span data-ttu-id="ad99d-126">KeyVault objektum</span><span class="sxs-lookup"><span data-stu-id="ad99d-126">KeyVault object</span></span>

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

### <span data-ttu-id="ad99d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad99d-127">-ResourceId</span></span>
<span data-ttu-id="ad99d-128">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="ad99d-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="ad99d-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ad99d-129">-VaultName</span></span>
<span data-ttu-id="ad99d-130">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="ad99d-130">Vault name.</span></span>
<span data-ttu-id="ad99d-131">A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="ad99d-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ad99d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad99d-132">-Confirm</span></span>
<span data-ttu-id="ad99d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ad99d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad99d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad99d-134">-WhatIf</span></span>
<span data-ttu-id="ad99d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ad99d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad99d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad99d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad99d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad99d-137">CommonParameters</span></span>
<span data-ttu-id="ad99d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad99d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad99d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad99d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad99d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad99d-140">INPUTS</span></span>

### <span data-ttu-id="ad99d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ad99d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ad99d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ad99d-142">System.String</span></span>

## <span data-ttu-id="ad99d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad99d-143">OUTPUTS</span></span>

### <span data-ttu-id="ad99d-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ad99d-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="ad99d-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad99d-145">NOTES</span></span>

## <span data-ttu-id="ad99d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad99d-146">RELATED LINKS</span></span>
