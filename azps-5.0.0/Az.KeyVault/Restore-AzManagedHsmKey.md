---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195911"
---
# <span data-ttu-id="184e9-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="184e9-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="184e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="184e9-102">SYNOPSIS</span></span>
<span data-ttu-id="184e9-103">A kezelt HSM kulcsát hozza létre egy biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="184e9-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="184e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="184e9-104">SYNTAX</span></span>

### <span data-ttu-id="184e9-105">ByHsmName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="184e9-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184e9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="184e9-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184e9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="184e9-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="184e9-108">DESCRIPTION</span></span>
<span data-ttu-id="184e9-109">A **Restore-AzManagedHsmKey** parancsmag létrehoz egy kulcsot a megadott felügyelt HSM-ben.</span><span class="sxs-lookup"><span data-stu-id="184e9-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="184e9-110">Ez a kulcs a bemeneti fájlban lévő mentett kulcs replikája, és az eredeti kulcs nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="184e9-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="184e9-111">Ha a felügyelt HSM már rendelkezik ugyanazzal a névvel, az eredeti kulcs felülírása helyett ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="184e9-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="184e9-112">Ha a biztonsági másolat több verziót tartalmaz, a rendszer visszaállítja az összes verziót.</span><span class="sxs-lookup"><span data-stu-id="184e9-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="184e9-113">A felügyelt HSM, amelynek a kulcsát vissza szeretné állítani, eltérhetnek a kezelt HSM-ből, amelyből biztonsági másolatot készített a kulcsról.</span><span class="sxs-lookup"><span data-stu-id="184e9-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="184e9-114">A felügyelt HSM-nek azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="184e9-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="184e9-115">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="184e9-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="184e9-116">Példák</span><span class="sxs-lookup"><span data-stu-id="184e9-116">EXAMPLES</span></span>

### <span data-ttu-id="184e9-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="184e9-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="184e9-118">Ez a parancs visszaállít egy billentyűt, benne az összes változatát, a Backup. blob nevű biztonsági másolatból a testmhsm nevű felügyelt HSM nevű fájlból.</span><span class="sxs-lookup"><span data-stu-id="184e9-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="184e9-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="184e9-119">PARAMETERS</span></span>

### <span data-ttu-id="184e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184e9-120">-DefaultProfile</span></span>
<span data-ttu-id="184e9-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="184e9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="184e9-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="184e9-122">-HsmName</span></span>
<span data-ttu-id="184e9-123">HSM-név.</span><span class="sxs-lookup"><span data-stu-id="184e9-123">HSM name.</span></span> <span data-ttu-id="184e9-124">A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.</span><span class="sxs-lookup"><span data-stu-id="184e9-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184e9-125">-InputFile</span><span class="sxs-lookup"><span data-stu-id="184e9-125">-InputFile</span></span>
<span data-ttu-id="184e9-126">Bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="184e9-126">Input file.</span></span>
<span data-ttu-id="184e9-127">A mentett blobot tartalmazó bemeneti fájl</span><span class="sxs-lookup"><span data-stu-id="184e9-127">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="184e9-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="184e9-128">-InputObject</span></span>
<span data-ttu-id="184e9-129">HSM-objektum</span><span class="sxs-lookup"><span data-stu-id="184e9-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="184e9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="184e9-130">-ResourceId</span></span>
<span data-ttu-id="184e9-131">HSM-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="184e9-131">HSM Resource Id</span></span>

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

### <span data-ttu-id="184e9-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="184e9-132">-Confirm</span></span>
<span data-ttu-id="184e9-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="184e9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="184e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184e9-134">-WhatIf</span></span>
<span data-ttu-id="184e9-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="184e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184e9-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="184e9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="184e9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184e9-137">CommonParameters</span></span>
<span data-ttu-id="184e9-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="184e9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184e9-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="184e9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184e9-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="184e9-140">INPUTS</span></span>

### <span data-ttu-id="184e9-141">Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="184e9-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="184e9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="184e9-142">System.String</span></span>

## <span data-ttu-id="184e9-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="184e9-143">OUTPUTS</span></span>

### <span data-ttu-id="184e9-144">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="184e9-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="184e9-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="184e9-145">NOTES</span></span>

## <span data-ttu-id="184e9-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="184e9-146">RELATED LINKS</span></span>

[<span data-ttu-id="184e9-147">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="184e9-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="184e9-148">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="184e9-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="184e9-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="184e9-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="184e9-150">Visszavonás – AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="184e9-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="184e9-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="184e9-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="184e9-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="184e9-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)