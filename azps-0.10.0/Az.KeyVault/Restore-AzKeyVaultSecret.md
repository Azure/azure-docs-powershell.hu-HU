---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843877"
---
# <span data-ttu-id="6bf52-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6bf52-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6bf52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6bf52-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf52-103">Titkos kulccsal elkészített titkos kulccsal hoz létre titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="6bf52-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="6bf52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6bf52-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bf52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6bf52-105">DESCRIPTION</span></span>
<span data-ttu-id="6bf52-106">A **Restore-AzKeyVaultSecret** parancsmag titkot hoz létre a megadott kulcs boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="6bf52-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="6bf52-107">Ez a titok a bemeneti fájlban lévő mentett titok másolata, és az eredeti titok nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="6bf52-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="6bf52-108">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, a parancsmag nem felülírja az eredeti titkot.</span><span class="sxs-lookup"><span data-stu-id="6bf52-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="6bf52-109">Ha a biztonsági másolat több titkos verziót tartalmaz, az összes verzió visszaállítása visszakerül.</span><span class="sxs-lookup"><span data-stu-id="6bf52-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="6bf52-110">A titkot visszaadó kulcsfájl eltérhet attól a fő boltozattól, amelyről biztonsági másolatot készített.</span><span class="sxs-lookup"><span data-stu-id="6bf52-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="6bf52-111">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="6bf52-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="6bf52-112">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="6bf52-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="6bf52-113">Példák</span><span class="sxs-lookup"><span data-stu-id="6bf52-113">EXAMPLES</span></span>

### <span data-ttu-id="6bf52-114">Példa 1: biztonsági mentett titok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="6bf52-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="6bf52-115">Ez a parancs visszaállítja a titkos verziót, benne az összes verzióját, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="6bf52-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="6bf52-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6bf52-116">PARAMETERS</span></span>

### <span data-ttu-id="6bf52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf52-117">-DefaultProfile</span></span>
<span data-ttu-id="6bf52-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6bf52-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bf52-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6bf52-119">-InputFile</span></span>
<span data-ttu-id="6bf52-120">Azt a bemeneti fájlt adja meg, amely a visszaállítandó titok biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6bf52-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="6bf52-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6bf52-121">-VaultName</span></span>
<span data-ttu-id="6bf52-122">Annak a kulcsnak a nevét adja meg, amelybe vissza szeretné állítani a titkot.</span><span class="sxs-lookup"><span data-stu-id="6bf52-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="6bf52-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6bf52-123">-Confirm</span></span>
<span data-ttu-id="6bf52-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6bf52-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bf52-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf52-125">-WhatIf</span></span>
<span data-ttu-id="6bf52-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6bf52-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bf52-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bf52-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bf52-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf52-128">CommonParameters</span></span>
<span data-ttu-id="6bf52-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6bf52-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf52-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bf52-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf52-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bf52-131">INPUTS</span></span>

### <span data-ttu-id="6bf52-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="6bf52-132">None</span></span>
<span data-ttu-id="6bf52-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6bf52-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6bf52-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bf52-134">OUTPUTS</span></span>

### <span data-ttu-id="6bf52-135">Microsoft. Azure. Command. kulccsal. modellek. Secret</span><span class="sxs-lookup"><span data-stu-id="6bf52-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="6bf52-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6bf52-136">NOTES</span></span>

## <span data-ttu-id="6bf52-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bf52-137">RELATED LINKS</span></span>

[<span data-ttu-id="6bf52-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6bf52-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="6bf52-139">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6bf52-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="6bf52-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6bf52-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="6bf52-141">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6bf52-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

