---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: e25cbbeb4f9920e468638bbae2ef8c53ca241fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672232"
---
# <span data-ttu-id="0eeaf-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0eeaf-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="0eeaf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0eeaf-102">SYNOPSIS</span></span>
<span data-ttu-id="0eeaf-103">Letiltja a biztonsági másolat védett elemeinek védelmét.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eeaf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0eeaf-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eeaf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0eeaf-105">DESCRIPTION</span></span>
<span data-ttu-id="0eeaf-106">A **disable-AzureRmBackupProtection** parancsmag letiltja az Azure Backup-védett elemek védelmét.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="0eeaf-107">Ez a parancsmag leállítja az elemek rendszeres ütemezett biztonsági mentését.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="0eeaf-108">Ez a parancsmag a biztonsági másolat meglévő helyreállítási pontját tudja törölni.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="0eeaf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0eeaf-109">EXAMPLES</span></span>

## <span data-ttu-id="0eeaf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-110">PARAMETERS</span></span>

### <span data-ttu-id="0eeaf-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0eeaf-111">-Force</span></span>
<span data-ttu-id="0eeaf-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0eeaf-113">-Elem</span><span class="sxs-lookup"><span data-stu-id="0eeaf-113">-Item</span></span>
<span data-ttu-id="0eeaf-114">Annak a biztonsági másolatnak az elemét adja meg, amelyre a parancsmag letiltja a védelmet.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-114">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="0eeaf-115">Ha **AzureRmBackupItem** szeretne beolvasni, használja az Get-AzureRmBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-115">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="0eeaf-116">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="0eeaf-116">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="0eeaf-117">Azt jelzi, hogy ez a parancsmag törli a meglévő helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-117">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="0eeaf-118">Ha később törölni szeretné a tárolt helyreállítási pontokat, futtassa újra ezt a parancsmagot, és adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-118">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="0eeaf-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0eeaf-119">-Confirm</span></span>
<span data-ttu-id="0eeaf-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eeaf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eeaf-121">-WhatIf</span></span>
<span data-ttu-id="0eeaf-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eeaf-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eeaf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eeaf-124">-DefaultProfile</span></span>
<span data-ttu-id="0eeaf-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0eeaf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eeaf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eeaf-126">CommonParameters</span></span>
<span data-ttu-id="0eeaf-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0eeaf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eeaf-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eeaf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eeaf-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-129">INPUTS</span></span>

### <span data-ttu-id="0eeaf-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="0eeaf-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="0eeaf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-131">OUTPUTS</span></span>

### <span data-ttu-id="0eeaf-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="0eeaf-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="0eeaf-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0eeaf-133">NOTES</span></span>

## <span data-ttu-id="0eeaf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0eeaf-134">RELATED LINKS</span></span>

[<span data-ttu-id="0eeaf-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0eeaf-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="0eeaf-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="0eeaf-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


