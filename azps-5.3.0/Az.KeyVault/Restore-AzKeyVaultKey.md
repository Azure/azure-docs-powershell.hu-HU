---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465956"
---
# <span data-ttu-id="2aca6-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2aca6-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="2aca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aca6-102">SYNOPSIS</span></span>
<span data-ttu-id="2aca6-103">Kulcsot hoz létre egy kulcstárban egy biztonságimentett kulcsból.</span><span class="sxs-lookup"><span data-stu-id="2aca6-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="2aca6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2aca6-104">SYNTAX</span></span>

### <span data-ttu-id="2aca6-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2aca6-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aca6-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="2aca6-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aca6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2aca6-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aca6-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="2aca6-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aca6-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2aca6-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aca6-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="2aca6-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aca6-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2aca6-111">DESCRIPTION</span></span>
<span data-ttu-id="2aca6-112">A **Restore-AzKeyVaultKey** parancsmag létrehoz egy kulcsot a megadott kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="2aca6-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="2aca6-113">Ez a kulcs a bemeneti fájlban található biztonsági másolat másolata, és neve megegyezik az eredeti kulcs nevével.</span><span class="sxs-lookup"><span data-stu-id="2aca6-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="2aca6-114">Ha a kulcstárnak már van ugyanaz a neve, a parancsmag nem tudja felülírni az eredeti kulcsot.</span><span class="sxs-lookup"><span data-stu-id="2aca6-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="2aca6-115">Ha a biztonsági másolat egy kulcs több verzióját tartalmazza, a rendszer az összes verziót visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="2aca6-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="2aca6-116">Az a kulcstár, amelybe visszaállítja a kulcsot, különbözik attól a kulcstártól, amelyről a kulcsot biztonsági másolatban tárolta.</span><span class="sxs-lookup"><span data-stu-id="2aca6-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="2aca6-117">A kulcstárnak azonban ugyanazt az előfizetést kell használnia, és ugyanabban a földrajzi régióban (például Észak-Amerikában) kell lennie egy Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="2aca6-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="2aca6-118">Az Azure-régiók földrajzokkal való megfeleltetését a Microsoft Azure Trust Center https://azure.microsoft.com/support/trust-center/) webhelyén tudja meg.</span><span class="sxs-lookup"><span data-stu-id="2aca6-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="2aca6-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2aca6-119">EXAMPLES</span></span>

### <span data-ttu-id="2aca6-120">1. példa: Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="2aca6-120">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="2aca6-121">Ez a parancs visszaállít egy kulcsot az összes verziójával együtt a Backup.blob nevű biztonságimásolat-fájlból a MyKeyVault nevű kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="2aca6-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="2aca6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2aca6-122">PARAMETERS</span></span>

### <span data-ttu-id="2aca6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aca6-123">-DefaultProfile</span></span>
<span data-ttu-id="2aca6-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2aca6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aca6-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="2aca6-125">-HsmName</span></span>
<span data-ttu-id="2aca6-126">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="2aca6-126">HSM name.</span></span> <span data-ttu-id="2aca6-127">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="2aca6-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aca6-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="2aca6-128">-HsmObject</span></span>
<span data-ttu-id="2aca6-129">HSM objektum</span><span class="sxs-lookup"><span data-stu-id="2aca6-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aca6-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="2aca6-130">-HsmResourceId</span></span>
<span data-ttu-id="2aca6-131">Hsm Resource Id</span><span class="sxs-lookup"><span data-stu-id="2aca6-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aca6-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="2aca6-132">-InputFile</span></span>
<span data-ttu-id="2aca6-133">A visszaállítani kívánt kulcs biztonsági másolatát tartalmazó bemeneti fájl.</span><span class="sxs-lookup"><span data-stu-id="2aca6-133">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="2aca6-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aca6-134">-InputObject</span></span>
<span data-ttu-id="2aca6-135">KeyVault objektum</span><span class="sxs-lookup"><span data-stu-id="2aca6-135">KeyVault object</span></span>

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

### <span data-ttu-id="2aca6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aca6-136">-ResourceId</span></span>
<span data-ttu-id="2aca6-137">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="2aca6-137">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="2aca6-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2aca6-138">-VaultName</span></span>
<span data-ttu-id="2aca6-139">Annak a kulcstárnak a nevét adja meg, amelybe vissza kell állítani a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="2aca6-139">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="2aca6-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2aca6-140">-Confirm</span></span>
<span data-ttu-id="2aca6-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2aca6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aca6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aca6-142">-WhatIf</span></span>
<span data-ttu-id="2aca6-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2aca6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aca6-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2aca6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aca6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aca6-145">CommonParameters</span></span>
<span data-ttu-id="2aca6-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aca6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aca6-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2aca6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aca6-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2aca6-148">INPUTS</span></span>

### <span data-ttu-id="2aca6-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2aca6-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="2aca6-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2aca6-150">System.String</span></span>

## <span data-ttu-id="2aca6-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aca6-151">OUTPUTS</span></span>

### <span data-ttu-id="2aca6-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2aca6-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="2aca6-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2aca6-153">NOTES</span></span>

## <span data-ttu-id="2aca6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2aca6-154">RELATED LINKS</span></span>

[<span data-ttu-id="2aca6-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2aca6-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="2aca6-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2aca6-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="2aca6-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2aca6-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="2aca6-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2aca6-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

