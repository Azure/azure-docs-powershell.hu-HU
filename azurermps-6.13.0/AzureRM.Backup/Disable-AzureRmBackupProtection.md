---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: ebea82628aae6df23d16a341f3fd503870a8037a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502247"
---
# <span data-ttu-id="c490a-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c490a-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="c490a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c490a-102">SYNOPSIS</span></span>
<span data-ttu-id="c490a-103">Letiltja a biztonsági másolat védett elemeinek védelmét.</span><span class="sxs-lookup"><span data-stu-id="c490a-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c490a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c490a-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c490a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c490a-105">DESCRIPTION</span></span>
<span data-ttu-id="c490a-106">A **disable-AzureRmBackupProtection** parancsmag letiltja az Azure Backup-védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="c490a-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="c490a-107">Ez a parancsmag leállítja az elemek rendszeres ütemezett biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="c490a-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="c490a-108">Ez a parancsmag a biztonsági másolat meglévő helyreállítási pontját tudja törölni.</span><span class="sxs-lookup"><span data-stu-id="c490a-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="c490a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c490a-109">EXAMPLES</span></span>

## <span data-ttu-id="c490a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c490a-110">PARAMETERS</span></span>

### <span data-ttu-id="c490a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c490a-111">-DefaultProfile</span></span>
<span data-ttu-id="c490a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c490a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c490a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c490a-113">-Force</span></span>
<span data-ttu-id="c490a-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c490a-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c490a-115">-Elem</span><span class="sxs-lookup"><span data-stu-id="c490a-115">-Item</span></span>
<span data-ttu-id="c490a-116">Annak a biztonsági másolatnak az elemét adja meg, amelyre a parancsmag letiltja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="c490a-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="c490a-117">Ha **AzureRmBackupItem** szeretne beolvasni, használja az Get-AzureRmBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c490a-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c490a-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="c490a-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="c490a-119">Azt jelzi, hogy ez a parancsmag törli a meglévő helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="c490a-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="c490a-120">Ha később törölni szeretné a tárolt helyreállítási pontokat, futtassa újra ezt a parancsmagot, és adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="c490a-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c490a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c490a-121">-Confirm</span></span>
<span data-ttu-id="c490a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c490a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c490a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c490a-123">-WhatIf</span></span>
<span data-ttu-id="c490a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c490a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c490a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c490a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c490a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c490a-126">CommonParameters</span></span>
<span data-ttu-id="c490a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c490a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c490a-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c490a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c490a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c490a-129">INPUTS</span></span>

### <span data-ttu-id="c490a-130">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="c490a-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="c490a-131">Paraméterek: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c490a-131">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="c490a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c490a-132">OUTPUTS</span></span>

### <span data-ttu-id="c490a-133">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="c490a-133">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="c490a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c490a-134">NOTES</span></span>

## <span data-ttu-id="c490a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c490a-135">RELATED LINKS</span></span>

[<span data-ttu-id="c490a-136">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c490a-136">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="c490a-137">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="c490a-137">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


