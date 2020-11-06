---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498936"
---
# <span data-ttu-id="8f139-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8f139-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="8f139-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f139-102">SYNOPSIS</span></span>
<span data-ttu-id="8f139-103">Titkos kulccsal elkészített titkos kulccsal hoz létre titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8f139-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f139-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f139-104">SYNTAX</span></span>

### <span data-ttu-id="8f139-105">ByVaultName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f139-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f139-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f139-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f139-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f139-107">DESCRIPTION</span></span>
<span data-ttu-id="8f139-108">A **Restore-AzureKeyVaultSecret** parancsmag titkot hoz létre a megadott kulcs boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="8f139-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="8f139-109">Ez a titok a bemeneti fájlban lévő mentett titok másolata, és az eredeti titok nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="8f139-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="8f139-110">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, a parancsmag nem felülírja az eredeti titkot.</span><span class="sxs-lookup"><span data-stu-id="8f139-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="8f139-111">Ha a biztonsági másolat több titkos verziót tartalmaz, az összes verzió visszaállítása visszakerül.</span><span class="sxs-lookup"><span data-stu-id="8f139-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="8f139-112">A titkot visszaadó kulcsfájl eltérhet attól a fő boltozattól, amelyről biztonsági másolatot készített.</span><span class="sxs-lookup"><span data-stu-id="8f139-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="8f139-113">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="8f139-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="8f139-114">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="8f139-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="8f139-115">Példák</span><span class="sxs-lookup"><span data-stu-id="8f139-115">EXAMPLES</span></span>

### <span data-ttu-id="8f139-116">Példa 1: biztonsági mentett titok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="8f139-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="8f139-117">Ez a parancs visszaállítja a titkos verziót, benne az összes verzióját, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="8f139-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="8f139-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f139-118">PARAMETERS</span></span>

### <span data-ttu-id="8f139-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f139-119">-DefaultProfile</span></span>
<span data-ttu-id="8f139-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8f139-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f139-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8f139-121">-InputFile</span></span>
<span data-ttu-id="8f139-122">Azt a bemeneti fájlt adja meg, amely a visszaállítandó titok biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8f139-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="8f139-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f139-123">-InputObject</span></span>
<span data-ttu-id="8f139-124">A boltozat objektum</span><span class="sxs-lookup"><span data-stu-id="8f139-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f139-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8f139-125">-VaultName</span></span>
<span data-ttu-id="8f139-126">Annak a kulcsnak a nevét adja meg, amelybe vissza szeretné állítani a titkot.</span><span class="sxs-lookup"><span data-stu-id="8f139-126">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f139-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f139-127">-Confirm</span></span>
<span data-ttu-id="8f139-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f139-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f139-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f139-129">-WhatIf</span></span>
<span data-ttu-id="8f139-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f139-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f139-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f139-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f139-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f139-132">CommonParameters</span></span>
<span data-ttu-id="8f139-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f139-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f139-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f139-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f139-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f139-135">INPUTS</span></span>

### <span data-ttu-id="8f139-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="8f139-136">None</span></span>
<span data-ttu-id="8f139-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8f139-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f139-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f139-138">OUTPUTS</span></span>

### <span data-ttu-id="8f139-139">Microsoft. Azure. Command. PSKeyVaultSecret. models.</span><span class="sxs-lookup"><span data-stu-id="8f139-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="8f139-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f139-140">NOTES</span></span>

## <span data-ttu-id="8f139-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f139-141">RELATED LINKS</span></span>

[<span data-ttu-id="8f139-142">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8f139-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="8f139-143">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8f139-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="8f139-144">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8f139-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="8f139-145">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8f139-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

