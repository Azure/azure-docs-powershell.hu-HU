---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: f578fa3aab2cf89dcb8d3a753855ded57eaf35db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679289"
---
# <span data-ttu-id="18a64-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18a64-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="18a64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18a64-102">SYNOPSIS</span></span>
<span data-ttu-id="18a64-103">A biztonságimásolat-boltozat tárolási típusának módosítása.</span><span class="sxs-lookup"><span data-stu-id="18a64-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18a64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18a64-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18a64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18a64-105">DESCRIPTION</span></span>
<span data-ttu-id="18a64-106">A **set-AzureRmBackupVault** parancsmag az Azure Backup Vault tárolási típusát módosítja.</span><span class="sxs-lookup"><span data-stu-id="18a64-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="18a64-107">A boltozat többi tulajdonságát nem módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="18a64-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="18a64-108">Példák</span><span class="sxs-lookup"><span data-stu-id="18a64-108">EXAMPLES</span></span>

### <span data-ttu-id="18a64-109">Példa 1: meglévő boltozat tárterületének módosítása</span><span class="sxs-lookup"><span data-stu-id="18a64-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="18a64-110">Ez a parancs a **Get-AzureRmBackupVault** parancsmaggal kapja meg a Vault03 nevű Azure Backup Vault nevet.</span><span class="sxs-lookup"><span data-stu-id="18a64-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="18a64-111">A parancs a pipeline operátorral továbbítja az aktuális parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="18a64-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="18a64-112">Az aktuális parancsmag a LocallyRedundant-ra módosítja a tárterület típusát.</span><span class="sxs-lookup"><span data-stu-id="18a64-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="18a64-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18a64-113">PARAMETERS</span></span>

### <span data-ttu-id="18a64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a64-114">-DefaultProfile</span></span>
<span data-ttu-id="18a64-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="18a64-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18a64-116">-Tárterület</span><span class="sxs-lookup"><span data-stu-id="18a64-116">-Storage</span></span>
<span data-ttu-id="18a64-117">A biztonsági másolat adatainak tárolási típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18a64-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="18a64-118">A paraméter elfogadható értékei a következők: LocallyRedundant és GeoRedundant.</span><span class="sxs-lookup"><span data-stu-id="18a64-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18a64-119">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="18a64-119">-Vault</span></span>
<span data-ttu-id="18a64-120">Megadja azt a biztonságimásolat-tárolót, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="18a64-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="18a64-121">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="18a64-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18a64-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a64-122">CommonParameters</span></span>
<span data-ttu-id="18a64-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18a64-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a64-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18a64-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a64-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18a64-125">INPUTS</span></span>

### <span data-ttu-id="18a64-126">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18a64-126">AzureRmBackupVault</span></span>

## <span data-ttu-id="18a64-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18a64-127">OUTPUTS</span></span>

### <span data-ttu-id="18a64-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="18a64-128">None</span></span>

## <span data-ttu-id="18a64-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18a64-129">NOTES</span></span>
* <span data-ttu-id="18a64-130">Amikor az első kiszolgálót vagy a virtuális gépet egy boltozathoz regisztrálja, a tároló típusa zárolva van.</span><span class="sxs-lookup"><span data-stu-id="18a64-130">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="18a64-131">Ezt követően nem módosíthatja a tárterület típusát.</span><span class="sxs-lookup"><span data-stu-id="18a64-131">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="18a64-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18a64-132">RELATED LINKS</span></span>

[<span data-ttu-id="18a64-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18a64-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="18a64-134">Új – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18a64-134">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="18a64-135">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18a64-135">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


