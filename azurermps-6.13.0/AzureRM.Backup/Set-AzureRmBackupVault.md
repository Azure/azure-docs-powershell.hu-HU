---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494172"
---
# <span data-ttu-id="0aca6-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0aca6-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="0aca6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0aca6-102">SYNOPSIS</span></span>
<span data-ttu-id="0aca6-103">A biztonságimásolat-boltozat tárolási típusának módosítása.</span><span class="sxs-lookup"><span data-stu-id="0aca6-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aca6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0aca6-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aca6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0aca6-105">DESCRIPTION</span></span>
<span data-ttu-id="0aca6-106">A **set-AzureRmBackupVault** parancsmag az Azure Backup Vault tárolási típusát módosítja.</span><span class="sxs-lookup"><span data-stu-id="0aca6-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="0aca6-107">A boltozat többi tulajdonságát nem módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="0aca6-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="0aca6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0aca6-108">EXAMPLES</span></span>

### <span data-ttu-id="0aca6-109">Példa 1: meglévő boltozat tárterületének módosítása</span><span class="sxs-lookup"><span data-stu-id="0aca6-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="0aca6-110">Ez a parancs a **Get-AzureRmBackupVault** parancsmaggal kapja meg a Vault03 nevű Azure Backup Vault nevet.</span><span class="sxs-lookup"><span data-stu-id="0aca6-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="0aca6-111">A parancs a pipeline operátorral továbbítja az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0aca6-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0aca6-112">Az aktuális parancsmag a LocallyRedundant-ra módosítja a tárterület típusát.</span><span class="sxs-lookup"><span data-stu-id="0aca6-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="0aca6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0aca6-113">PARAMETERS</span></span>

### <span data-ttu-id="0aca6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aca6-114">-DefaultProfile</span></span>
<span data-ttu-id="0aca6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0aca6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0aca6-116">-Tárterület</span><span class="sxs-lookup"><span data-stu-id="0aca6-116">-Storage</span></span>
<span data-ttu-id="0aca6-117">A biztonsági másolat adatainak tárolási típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0aca6-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="0aca6-118">A paraméter elfogadható értékei a következők: LocallyRedundant és GeoRedundant.</span><span class="sxs-lookup"><span data-stu-id="0aca6-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aca6-119">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="0aca6-119">-Vault</span></span>
<span data-ttu-id="0aca6-120">Megadja azt a biztonságimásolat-tárolót, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="0aca6-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="0aca6-121">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0aca6-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="0aca6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aca6-122">CommonParameters</span></span>
<span data-ttu-id="0aca6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0aca6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aca6-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aca6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aca6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0aca6-125">INPUTS</span></span>

### <span data-ttu-id="0aca6-126">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="0aca6-126">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="0aca6-127">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0aca6-127">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="0aca6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0aca6-128">OUTPUTS</span></span>

### <span data-ttu-id="0aca6-129">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="0aca6-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="0aca6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0aca6-130">NOTES</span></span>
* <span data-ttu-id="0aca6-131">Amikor az első kiszolgálót vagy a virtuális gépet egy boltozathoz regisztrálja, a tároló típusa zárolva van.</span><span class="sxs-lookup"><span data-stu-id="0aca6-131">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="0aca6-132">Ezt követően nem módosíthatja a tárterület típusát.</span><span class="sxs-lookup"><span data-stu-id="0aca6-132">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="0aca6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0aca6-133">RELATED LINKS</span></span>

[<span data-ttu-id="0aca6-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0aca6-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="0aca6-135">Új – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0aca6-135">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="0aca6-136">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0aca6-136">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


