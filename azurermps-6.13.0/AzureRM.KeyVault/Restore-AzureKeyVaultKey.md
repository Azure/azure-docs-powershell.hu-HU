---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 70c56aaee4bf6547ad932965a190d3ecb2d93f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493682"
---
# <span data-ttu-id="4ca8d-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ca8d-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="4ca8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ca8d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca8d-103">Egy kulccsal létrehozott billentyűt hoz létre egy biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ca8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ca8d-104">SYNTAX</span></span>

### <span data-ttu-id="4ca8d-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ca8d-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca8d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ca8d-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca8d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca8d-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultKey [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ca8d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ca8d-108">DESCRIPTION</span></span>
<span data-ttu-id="4ca8d-109">A **Restore-AzureKeyVaultKey** parancsmag egy kulcsot hoz létre a megadott kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-109">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="4ca8d-110">Ez a kulcs a bemeneti fájlban lévő mentett kulcs replikája, és az eredeti kulcs nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="4ca8d-111">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, az eredeti kulcs felülírása helyett ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="4ca8d-112">Ha a biztonsági másolat több verziót tartalmaz, a rendszer visszaállítja az összes verziót.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="4ca8d-113">Annak a kulcsnak a boltozata, amelynek a kulcsát vissza szeretné állítani, eltérhet a kulcs boltozattól.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="4ca8d-114">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="4ca8d-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="4ca8d-115">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="4ca8d-116">Példák</span><span class="sxs-lookup"><span data-stu-id="4ca8d-116">EXAMPLES</span></span>

### <span data-ttu-id="4ca8d-117">Példa 1: biztonsági mentett kulcs visszaállítása</span><span class="sxs-lookup"><span data-stu-id="4ca8d-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="4ca8d-118">Ez a parancs visszaállít egy billentyűt, benne az összes verziót, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="4ca8d-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ca8d-119">PARAMETERS</span></span>

### <span data-ttu-id="4ca8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca8d-120">-DefaultProfile</span></span>
<span data-ttu-id="4ca8d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4ca8d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ca8d-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4ca8d-122">-InputFile</span></span>
<span data-ttu-id="4ca8d-123">Azt a bemeneti fájlt adja meg, amely a visszaállítandó kulcs biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="4ca8d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ca8d-124">-InputObject</span></span>
<span data-ttu-id="4ca8d-125">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="4ca8d-125">KeyVault object</span></span>

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

### <span data-ttu-id="4ca8d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca8d-126">-ResourceId</span></span>
<span data-ttu-id="4ca8d-127">A főkészlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4ca8d-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="4ca8d-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ca8d-128">-VaultName</span></span>
<span data-ttu-id="4ca8d-129">Annak a kulcsnak a neve, amelybe vissza szeretné állítani a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="4ca8d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ca8d-130">-Confirm</span></span>
<span data-ttu-id="4ca8d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ca8d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca8d-132">-WhatIf</span></span>
<span data-ttu-id="4ca8d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ca8d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ca8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca8d-135">CommonParameters</span></span>
<span data-ttu-id="4ca8d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ca8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca8d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca8d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca8d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ca8d-138">INPUTS</span></span>

### <span data-ttu-id="4ca8d-139">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="4ca8d-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ca8d-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4ca8d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4ca8d-141">System.String</span></span>

## <span data-ttu-id="4ca8d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ca8d-142">OUTPUTS</span></span>

### <span data-ttu-id="4ca8d-143">Microsoft. Azure. Command. PSKeyVaultKey. models.</span><span class="sxs-lookup"><span data-stu-id="4ca8d-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="4ca8d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ca8d-144">NOTES</span></span>

## <span data-ttu-id="4ca8d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ca8d-145">RELATED LINKS</span></span>

[<span data-ttu-id="4ca8d-146">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ca8d-146">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="4ca8d-147">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ca8d-147">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="4ca8d-148">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ca8d-148">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="4ca8d-149">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ca8d-149">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

