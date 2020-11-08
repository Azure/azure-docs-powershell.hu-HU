---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010885"
---
# <span data-ttu-id="82649-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="82649-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="82649-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82649-102">SYNOPSIS</span></span>
<span data-ttu-id="82649-103">Megkapja a SCDPM és az Azure Backup Management kiszolgálókat.</span><span class="sxs-lookup"><span data-stu-id="82649-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="82649-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82649-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82649-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82649-105">DESCRIPTION</span></span>
<span data-ttu-id="82649-106">A **Get-AzRecoveryServicesBackupManagementServer** parancsmag a boltívben regisztrált biztonságimásolat-kezelési kiszolgálók listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="82649-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="82649-107">A biztonságimásolat-kezelési kiszolgálók két típusa van: a System Center Data Protection Manager (SCDPM) és az Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="82649-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="82649-108">A biztonságimásolat-kezelési kiszolgálók külön vannak telepítve a biztonságimásolat-hangszerelések kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="82649-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="82649-109">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="82649-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="82649-110">Példák</span><span class="sxs-lookup"><span data-stu-id="82649-110">EXAMPLES</span></span>

### <span data-ttu-id="82649-111">Példa 1: a biztonsági másolatok kezelésének összes kiszolgálójának beolvasása</span><span class="sxs-lookup"><span data-stu-id="82649-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="82649-112">Ez a parancs a boltozattal regisztrált összes biztonságimásolat-kezelési kiszolgálót megkapja.</span><span class="sxs-lookup"><span data-stu-id="82649-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="82649-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82649-113">PARAMETERS</span></span>

### <span data-ttu-id="82649-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82649-114">-DefaultProfile</span></span>
<span data-ttu-id="82649-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82649-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82649-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82649-116">-Name</span></span>
<span data-ttu-id="82649-117">A beolvasott biztonságimásolat-kezelési kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82649-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="82649-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="82649-118">-VaultId</span></span>
<span data-ttu-id="82649-119">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="82649-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="82649-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82649-120">CommonParameters</span></span>
<span data-ttu-id="82649-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82649-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82649-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="82649-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82649-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82649-123">INPUTS</span></span>

### <span data-ttu-id="82649-124">System. String</span><span class="sxs-lookup"><span data-stu-id="82649-124">System.String</span></span>

## <span data-ttu-id="82649-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82649-125">OUTPUTS</span></span>

### <span data-ttu-id="82649-126">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="82649-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="82649-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82649-127">NOTES</span></span>

## <span data-ttu-id="82649-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82649-128">RELATED LINKS</span></span>

[<span data-ttu-id="82649-129">Regisztráció törlése – AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="82649-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


