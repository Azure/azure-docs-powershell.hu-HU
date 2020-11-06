---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 1fb58d348af5f507e1bd3c8451f12918c69b309b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504912"
---
# <span data-ttu-id="5fe9f-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5fe9f-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="5fe9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fe9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe9f-103">Egy kulccsal létrehozott billentyűt hoz létre egy biztonsági másolatból.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fe9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fe9f-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fe9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fe9f-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe9f-106">A **Restore-AzureKeyVaultKey** parancsmag egy kulcsot hoz létre a megadott kulcs boltozatához.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="5fe9f-107">Ez a kulcs a bemeneti fájlban lévő mentett kulcs replikája, és az eredeti kulcs nevével megegyező.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="5fe9f-108">Ha a kulcs boltozata már rendelkezik ugyanazzal a névvel, az eredeti kulcs felülírása helyett ez a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="5fe9f-109">Ha a biztonsági másolat több verziót tartalmaz, a rendszer visszaállítja az összes verziót.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="5fe9f-110">Annak a kulcsnak a boltozata, amelynek a kulcsát vissza szeretné állítani, eltérhet a kulcs boltozattól.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="5fe9f-111">A kulcs boltozatának azonban ugyanazt az előfizetést kell használnia, és egy Azure-régióban kell lennie ugyanazon a földrajzon (például Észak-Amerikában).</span><span class="sxs-lookup"><span data-stu-id="5fe9f-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="5fe9f-112">Lásd: a Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) Az Azure-régiók földrajzi megfeleltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="5fe9f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5fe9f-113">EXAMPLES</span></span>

### <span data-ttu-id="5fe9f-114">Példa 1: biztonsági mentett kulcs visszaállítása</span><span class="sxs-lookup"><span data-stu-id="5fe9f-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="5fe9f-115">Ez a parancs visszaállít egy billentyűt, benne az összes verziót, a Backup. blob nevű biztonsági másolatból a MyKeyVault nevű kulcs boltozatát.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="5fe9f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fe9f-116">PARAMETERS</span></span>

### <span data-ttu-id="5fe9f-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5fe9f-117">-InputFile</span></span>
<span data-ttu-id="5fe9f-118">Azt a bemeneti fájlt adja meg, amely a visszaállítandó kulcs biztonsági másolatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-118">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9f-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5fe9f-119">-VaultName</span></span>
<span data-ttu-id="5fe9f-120">Annak a kulcsnak a neve, amelybe vissza szeretné állítani a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-120">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fe9f-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fe9f-121">-Confirm</span></span>
<span data-ttu-id="5fe9f-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe9f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe9f-123">-WhatIf</span></span>
<span data-ttu-id="5fe9f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe9f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe9f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe9f-126">-DefaultProfile</span></span>
<span data-ttu-id="5fe9f-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fe9f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fe9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe9f-128">CommonParameters</span></span>
<span data-ttu-id="5fe9f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fe9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe9f-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe9f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe9f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe9f-131">INPUTS</span></span>

## <span data-ttu-id="5fe9f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fe9f-132">OUTPUTS</span></span>

### <span data-ttu-id="5fe9f-133">Microsoft. Azure. Command. Vault. models. Bundle</span><span class="sxs-lookup"><span data-stu-id="5fe9f-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="5fe9f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fe9f-134">NOTES</span></span>

## <span data-ttu-id="5fe9f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fe9f-135">RELATED LINKS</span></span>

[<span data-ttu-id="5fe9f-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5fe9f-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="5fe9f-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5fe9f-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="5fe9f-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5fe9f-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="5fe9f-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5fe9f-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

