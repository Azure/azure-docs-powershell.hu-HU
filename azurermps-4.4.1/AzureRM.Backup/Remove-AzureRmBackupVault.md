---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 8530dbff2e348f1b068afe7293cae9c993ce064e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497916"
---
# <span data-ttu-id="64232-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="64232-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="64232-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64232-102">SYNOPSIS</span></span>
<span data-ttu-id="64232-103">Törli a biztonsági másolatot tároló boltozatot.</span><span class="sxs-lookup"><span data-stu-id="64232-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64232-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64232-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64232-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64232-105">DESCRIPTION</span></span>
<span data-ttu-id="64232-106">A **Remove-AzureRmBackupVault** parancsmag egy Azure Backup boltozatot töröl.</span><span class="sxs-lookup"><span data-stu-id="64232-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="64232-107">A biztonságimásolat-tároló törlése előtt üresnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="64232-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="64232-108">A **Remove-AzureRmBackupContainer** parancsmaggal eltávolíthatja az infrastruktúrát szolgáltatásként (IaaS) virtuális gép biztonsági mentési adatainak a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="64232-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="64232-109">A **delete-RegisteredServer** parancsmaggal további regisztrált kiszolgálókat és biztonsági másolatokat távolíthat el.</span><span class="sxs-lookup"><span data-stu-id="64232-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="64232-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64232-110">EXAMPLES</span></span>

### <span data-ttu-id="64232-111">Példa 1: Azure Backup Vault törlése</span><span class="sxs-lookup"><span data-stu-id="64232-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="64232-112">Ez a parancs a **Get-AzureRmBackupVault** parancsmaggal kapja meg a Vault03 nevű Azure Backup Vault nevet.</span><span class="sxs-lookup"><span data-stu-id="64232-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="64232-113">A parancs a pipeline operátorral továbbítja az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="64232-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="64232-114">Az aktuális parancsmag eltávolítja a boltozatot.</span><span class="sxs-lookup"><span data-stu-id="64232-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="64232-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64232-115">PARAMETERS</span></span>

### <span data-ttu-id="64232-116">-Force</span><span class="sxs-lookup"><span data-stu-id="64232-116">-Force</span></span>
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

### <span data-ttu-id="64232-117">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="64232-117">-Vault</span></span>
<span data-ttu-id="64232-118">Itt adhatja meg azt a biztonságimásolat-tárolót, amely a parancsmag eltávolítását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="64232-118">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="64232-119">Ha **AzureRmBackupVault** szeretne beolvasni, használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="64232-119">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64232-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64232-120">-Confirm</span></span>
<span data-ttu-id="64232-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64232-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64232-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64232-122">-WhatIf</span></span>
<span data-ttu-id="64232-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64232-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64232-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64232-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64232-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64232-125">-DefaultProfile</span></span>
<span data-ttu-id="64232-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64232-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64232-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64232-127">CommonParameters</span></span>
<span data-ttu-id="64232-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64232-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64232-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64232-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64232-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64232-130">INPUTS</span></span>

### <span data-ttu-id="64232-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="64232-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="64232-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64232-132">OUTPUTS</span></span>

### <span data-ttu-id="64232-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="64232-133">None</span></span>

## <span data-ttu-id="64232-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64232-134">NOTES</span></span>
* <span data-ttu-id="64232-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="64232-135">None</span></span>

## <span data-ttu-id="64232-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64232-136">RELATED LINKS</span></span>

[<span data-ttu-id="64232-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="64232-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="64232-138">Új – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="64232-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="64232-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="64232-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


