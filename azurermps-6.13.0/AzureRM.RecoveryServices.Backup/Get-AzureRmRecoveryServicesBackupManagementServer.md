---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c3419f020aca0853d94d8848e944e39fc8ed05a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495772"
---
# <span data-ttu-id="691b6-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="691b6-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="691b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="691b6-102">SYNOPSIS</span></span>
<span data-ttu-id="691b6-103">Megkapja a SCDPM és az Azure Backup Management kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="691b6-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="691b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="691b6-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="691b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="691b6-105">DESCRIPTION</span></span>
<span data-ttu-id="691b6-106">A **Get-AzureRmRecoveryServicesBackupManagementServer** parancsmag a boltívben regisztrált biztonságimásolat-kezelési kiszolgálók listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="691b6-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="691b6-107">A biztonságimásolat-kezelési kiszolgálók két típusa van: a System Center Data Protection Manager (SCDPM) és az Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="691b6-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="691b6-108">A biztonságimásolat-kezelési kiszolgálók külön vannak telepítve a biztonságimásolat-hangszerelések kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="691b6-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="691b6-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="691b6-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="691b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="691b6-110">EXAMPLES</span></span>

### <span data-ttu-id="691b6-111">Példa 1: a biztonsági másolatok kezelésének összes kiszolgálójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="691b6-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="691b6-112">Ez a parancs a boltozattal regisztrált összes biztonságimásolat-kezelési kiszolgálót megkapja.</span><span class="sxs-lookup"><span data-stu-id="691b6-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="691b6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="691b6-113">PARAMETERS</span></span>

### <span data-ttu-id="691b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691b6-114">-DefaultProfile</span></span>
<span data-ttu-id="691b6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="691b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="691b6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="691b6-116">-Name</span></span>
<span data-ttu-id="691b6-117">A beolvasott biztonságimásolat-kezelési kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="691b6-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691b6-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="691b6-118">-VaultId</span></span>
<span data-ttu-id="691b6-119">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="691b6-119">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="691b6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691b6-120">CommonParameters</span></span>
<span data-ttu-id="691b6-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="691b6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691b6-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691b6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691b6-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="691b6-123">INPUTS</span></span>

### <span data-ttu-id="691b6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="691b6-124">System.String</span></span>
<span data-ttu-id="691b6-125">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="691b6-125">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="691b6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="691b6-126">OUTPUTS</span></span>

### <span data-ttu-id="691b6-127">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="691b6-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="691b6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="691b6-128">NOTES</span></span>

## <span data-ttu-id="691b6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="691b6-129">RELATED LINKS</span></span>

[<span data-ttu-id="691b6-130">Regisztráció törlése – AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="691b6-130">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


