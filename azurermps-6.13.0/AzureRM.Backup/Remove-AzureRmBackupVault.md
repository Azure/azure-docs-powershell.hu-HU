---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 883c4a9892f4525b15369dbb1c3ed6134eb29f00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494182"
---
# <span data-ttu-id="d98e5-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d98e5-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="d98e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d98e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d98e5-103">Törli a biztonsági másolatot tároló boltozatot.</span><span class="sxs-lookup"><span data-stu-id="d98e5-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d98e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d98e5-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d98e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d98e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d98e5-106">A **Remove-AzureRmBackupVault** parancsmag egy Azure Backup boltozatot töröl.</span><span class="sxs-lookup"><span data-stu-id="d98e5-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>
<span data-ttu-id="d98e5-107">A biztonságimásolat-tároló törlése előtt üresnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d98e5-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="d98e5-108">A **Remove-AzureRmBackupContainer** parancsmaggal eltávolíthatja az infrastruktúrát szolgáltatásként (IaaS) virtuális gép biztonsági mentési adatainak a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="d98e5-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="d98e5-109">A **delete-RegisteredServer** parancsmaggal további regisztrált kiszolgálókat és biztonsági másolatokat távolíthat el.</span><span class="sxs-lookup"><span data-stu-id="d98e5-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="d98e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d98e5-110">EXAMPLES</span></span>

### <span data-ttu-id="d98e5-111">Példa 1: Azure Backup Vault törlése</span><span class="sxs-lookup"><span data-stu-id="d98e5-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="d98e5-112">Ez a parancs a **Get-AzureRmBackupVault** parancsmaggal kapja meg a Vault03 nevű Azure Backup Vault nevet.</span><span class="sxs-lookup"><span data-stu-id="d98e5-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="d98e5-113">A parancs a pipeline operátorral továbbítja az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d98e5-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d98e5-114">Az aktuális parancsmag eltávolítja a boltozatot.</span><span class="sxs-lookup"><span data-stu-id="d98e5-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="d98e5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d98e5-115">PARAMETERS</span></span>

### <span data-ttu-id="d98e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98e5-116">-DefaultProfile</span></span>
<span data-ttu-id="d98e5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d98e5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d98e5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d98e5-118">-Force</span></span>
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

### <span data-ttu-id="d98e5-119">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="d98e5-119">-Vault</span></span>
<span data-ttu-id="d98e5-120">Itt adhatja meg azt a biztonságimásolat-tárolót, amely a parancsmag eltávolítását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d98e5-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="d98e5-121">Ha **AzureRmBackupVault** szeretne beolvasni, használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d98e5-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="d98e5-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d98e5-122">-Confirm</span></span>
<span data-ttu-id="d98e5-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d98e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d98e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d98e5-124">-WhatIf</span></span>
<span data-ttu-id="d98e5-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d98e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d98e5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d98e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d98e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98e5-127">CommonParameters</span></span>
<span data-ttu-id="d98e5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d98e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98e5-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d98e5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98e5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d98e5-130">INPUTS</span></span>

### <span data-ttu-id="d98e5-131">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="d98e5-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="d98e5-132">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d98e5-132">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="d98e5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d98e5-133">OUTPUTS</span></span>

### <span data-ttu-id="d98e5-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="d98e5-134">System.Void</span></span>

## <span data-ttu-id="d98e5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d98e5-135">NOTES</span></span>
* <span data-ttu-id="d98e5-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="d98e5-136">None</span></span>

## <span data-ttu-id="d98e5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d98e5-137">RELATED LINKS</span></span>

[<span data-ttu-id="d98e5-138">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d98e5-138">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="d98e5-139">Új – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d98e5-139">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="d98e5-140">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d98e5-140">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


