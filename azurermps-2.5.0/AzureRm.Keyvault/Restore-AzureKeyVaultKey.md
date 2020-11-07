---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7bad1311d463b8372d07a33c549682a2cade4041
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848198"
---
# <span data-ttu-id="6fdc3-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6fdc3-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="6fdc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fdc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdc3-103">Egy kulccsal létrehozott billentyűt hoz létre egy biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fdc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fdc3-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fdc3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fdc3-105">DESCRIPTION</span></span>
<span data-ttu-id="6fdc3-106">A **Restore-AzureKeyVaultKey** parancsmag egy kulcsot hoz létre a megadott kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="6fdc3-107">Ez a kulcs a bemeneti fájlban lévő mentett kulcs replikája, és az eredeti kulcs nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="6fdc3-108">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, az eredeti kulcs felülírása helyett ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="6fdc3-109">Ha a biztonsági másolat több verziót tartalmaz, a rendszer visszaállítja az összes verziót.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="6fdc3-110">Annak a kulcsnak a boltozata, amelynek a kulcsát vissza szeretné állítani, eltérhet a kulcs boltozattól.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="6fdc3-111">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="6fdc3-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="6fdc3-112">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="6fdc3-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6fdc3-113">EXAMPLES</span></span>

### <span data-ttu-id="6fdc3-114">Példa 1: biztonsági mentett kulcs visszaállítása</span><span class="sxs-lookup"><span data-stu-id="6fdc3-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="6fdc3-115">Ez a parancs visszaállít egy billentyűt, benne az összes verziót, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="6fdc3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fdc3-116">PARAMETERS</span></span>

### <span data-ttu-id="6fdc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdc3-117">-DefaultProfile</span></span>
<span data-ttu-id="6fdc3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6fdc3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fdc3-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6fdc3-119">-InputFile</span></span>
<span data-ttu-id="6fdc3-120">Azt a bemeneti fájlt adja meg, amely a visszaállítandó kulcs biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-120">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdc3-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6fdc3-121">-VaultName</span></span>
<span data-ttu-id="6fdc3-122">Annak a kulcsnak a neve, amelybe vissza szeretné állítani a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="6fdc3-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6fdc3-123">-Confirm</span></span>
<span data-ttu-id="6fdc3-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fdc3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fdc3-125">-WhatIf</span></span>
<span data-ttu-id="6fdc3-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fdc3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fdc3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdc3-128">CommonParameters</span></span>
<span data-ttu-id="6fdc3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fdc3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdc3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fdc3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdc3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fdc3-131">INPUTS</span></span>

## <span data-ttu-id="6fdc3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fdc3-132">OUTPUTS</span></span>

### <span data-ttu-id="6fdc3-133">Microsoft. Azure. Command. Vault. models. Bundle</span><span class="sxs-lookup"><span data-stu-id="6fdc3-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="6fdc3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fdc3-134">NOTES</span></span>

## <span data-ttu-id="6fdc3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fdc3-135">RELATED LINKS</span></span>

[<span data-ttu-id="6fdc3-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6fdc3-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="6fdc3-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6fdc3-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="6fdc3-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6fdc3-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="6fdc3-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6fdc3-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
