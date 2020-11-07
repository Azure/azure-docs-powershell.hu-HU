---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: b8ce1dc13204cfeeb63f5b7eb45f57e2117da511
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848197"
---
# <span data-ttu-id="79c1c-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="79c1c-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="79c1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="79c1c-103">Titkos kulccsal elkészített titkos kulccsal hoz létre titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="79c1c-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79c1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79c1c-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c1c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="79c1c-106">A **Restore-AzureKeyVaultSecret** parancsmag titkot hoz létre a megadott kulcs boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="79c1c-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="79c1c-107">Ez a titok a bemeneti fájlban lévő mentett titok másolata, és az eredeti titok nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="79c1c-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="79c1c-108">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, a parancsmag nem felülírja az eredeti titkot.</span><span class="sxs-lookup"><span data-stu-id="79c1c-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="79c1c-109">Ha a biztonsági másolat több titkos verziót tartalmaz, az összes verzió visszaállítása visszakerül.</span><span class="sxs-lookup"><span data-stu-id="79c1c-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="79c1c-110">A titkot visszaadó kulcsfájl eltérhet attól a fő boltozattól, amelyről biztonsági másolatot készített.</span><span class="sxs-lookup"><span data-stu-id="79c1c-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="79c1c-111">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="79c1c-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="79c1c-112">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="79c1c-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="79c1c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="79c1c-113">EXAMPLES</span></span>

### <span data-ttu-id="79c1c-114">Példa 1: biztonsági mentett titok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="79c1c-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="79c1c-115">Ez a parancs visszaállítja a titkos verziót, benne az összes verzióját, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="79c1c-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="79c1c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79c1c-116">PARAMETERS</span></span>

### <span data-ttu-id="79c1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c1c-117">-DefaultProfile</span></span>
<span data-ttu-id="79c1c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79c1c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79c1c-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="79c1c-119">-InputFile</span></span>
<span data-ttu-id="79c1c-120">Azt a bemeneti fájlt adja meg, amely a visszaállítandó titok biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="79c1c-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="79c1c-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="79c1c-121">-VaultName</span></span>
<span data-ttu-id="79c1c-122">Annak a kulcsnak a nevét adja meg, amelybe vissza szeretné állítani a titkot.</span><span class="sxs-lookup"><span data-stu-id="79c1c-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="79c1c-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79c1c-123">-Confirm</span></span>
<span data-ttu-id="79c1c-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79c1c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c1c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c1c-125">-WhatIf</span></span>
<span data-ttu-id="79c1c-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79c1c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c1c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79c1c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c1c-128">CommonParameters</span></span>
<span data-ttu-id="79c1c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79c1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c1c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c1c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79c1c-131">INPUTS</span></span>

## <span data-ttu-id="79c1c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79c1c-132">OUTPUTS</span></span>

### <span data-ttu-id="79c1c-133">Microsoft. Azure. Command. kulccsal. modellek. Secret</span><span class="sxs-lookup"><span data-stu-id="79c1c-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="79c1c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79c1c-134">NOTES</span></span>

## <span data-ttu-id="79c1c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79c1c-135">RELATED LINKS</span></span>

[<span data-ttu-id="79c1c-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="79c1c-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="79c1c-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="79c1c-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="79c1c-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="79c1c-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="79c1c-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="79c1c-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

