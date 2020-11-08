---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185287"
---
# <span data-ttu-id="02c60-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="02c60-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="02c60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02c60-102">SYNOPSIS</span></span>
<span data-ttu-id="02c60-103">Egy kulccsal létrehozott billentyűt hoz létre egy biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="02c60-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="02c60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02c60-104">SYNTAX</span></span>

### <span data-ttu-id="02c60-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02c60-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c60-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="02c60-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c60-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02c60-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c60-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="02c60-108">DESCRIPTION</span></span>
<span data-ttu-id="02c60-109">A **Restore-AzKeyVaultKey** parancsmag egy kulcsot hoz létre a megadott kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="02c60-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="02c60-110">Ez a kulcs a bemeneti fájlban lévő mentett kulcs replikája, és az eredeti kulcs nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="02c60-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="02c60-111">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, az eredeti kulcs felülírása helyett ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="02c60-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="02c60-112">Ha a biztonsági másolat több verziót tartalmaz, a rendszer visszaállítja az összes verziót.</span><span class="sxs-lookup"><span data-stu-id="02c60-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="02c60-113">Annak a kulcsnak a boltozata, amelynek a kulcsát vissza szeretné állítani, eltérhet a kulcs boltozattól.</span><span class="sxs-lookup"><span data-stu-id="02c60-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="02c60-114">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="02c60-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="02c60-115">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="02c60-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="02c60-116">Példák</span><span class="sxs-lookup"><span data-stu-id="02c60-116">EXAMPLES</span></span>

### <span data-ttu-id="02c60-117">Példa 1: biztonsági mentett kulcs visszaállítása</span><span class="sxs-lookup"><span data-stu-id="02c60-117">Example 1: Restore a backed-up key</span></span>
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

<span data-ttu-id="02c60-118">Ez a parancs visszaállít egy billentyűt, benne az összes verziót, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="02c60-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="02c60-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02c60-119">PARAMETERS</span></span>

### <span data-ttu-id="02c60-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c60-120">-DefaultProfile</span></span>
<span data-ttu-id="02c60-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="02c60-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02c60-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="02c60-122">-InputFile</span></span>
<span data-ttu-id="02c60-123">Azt a bemeneti fájlt adja meg, amely a visszaállítandó kulcs biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="02c60-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="02c60-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c60-124">-InputObject</span></span>
<span data-ttu-id="02c60-125">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="02c60-125">KeyVault object</span></span>

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

### <span data-ttu-id="02c60-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02c60-126">-ResourceId</span></span>
<span data-ttu-id="02c60-127">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="02c60-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="02c60-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="02c60-128">-VaultName</span></span>
<span data-ttu-id="02c60-129">Annak a kulcsnak a neve, amelybe vissza szeretné állítani a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="02c60-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="02c60-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02c60-130">-Confirm</span></span>
<span data-ttu-id="02c60-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02c60-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c60-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c60-132">-WhatIf</span></span>
<span data-ttu-id="02c60-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02c60-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c60-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02c60-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c60-135">CommonParameters</span></span>
<span data-ttu-id="02c60-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02c60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c60-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="02c60-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c60-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02c60-138">INPUTS</span></span>

### <span data-ttu-id="02c60-139">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="02c60-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="02c60-140">System. String</span><span class="sxs-lookup"><span data-stu-id="02c60-140">System.String</span></span>

## <span data-ttu-id="02c60-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02c60-141">OUTPUTS</span></span>

### <span data-ttu-id="02c60-142">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="02c60-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="02c60-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02c60-143">NOTES</span></span>

## <span data-ttu-id="02c60-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02c60-144">RELATED LINKS</span></span>

[<span data-ttu-id="02c60-145">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="02c60-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="02c60-146">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="02c60-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="02c60-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="02c60-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="02c60-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="02c60-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)
