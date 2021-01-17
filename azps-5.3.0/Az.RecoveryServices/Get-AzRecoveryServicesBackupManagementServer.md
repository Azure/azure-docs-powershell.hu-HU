---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376654"
---
# <span data-ttu-id="38a5a-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="38a5a-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="38a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="38a5a-103">Az SCDPM és az Azure backup management servers leküldi.</span><span class="sxs-lookup"><span data-stu-id="38a5a-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="38a5a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38a5a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a5a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="38a5a-106">A **Get-AzRecoveryServicesBackupManagementServer** parancsmag lekérte a tárolóban regisztrált biztonságimásolat-kezelő kiszolgálók listáját.</span><span class="sxs-lookup"><span data-stu-id="38a5a-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="38a5a-107">A biztonságimásolat-kezelő kiszolgálóknak két típusa létezik: a System Center Data Protection Manager (SCDPM) és az Azure Backup management servers.</span><span class="sxs-lookup"><span data-stu-id="38a5a-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="38a5a-108">A biztonságimásolat-kezelő kiszolgálókat külön kell telepíteni a biztonsági másolatok kierőletelésének kezelésére.</span><span class="sxs-lookup"><span data-stu-id="38a5a-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="38a5a-109">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="38a5a-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="38a5a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38a5a-110">EXAMPLES</span></span>

### <span data-ttu-id="38a5a-111">1. példa: Az összes biztonsági mentést kezelő kiszolgáló lekérte</span><span class="sxs-lookup"><span data-stu-id="38a5a-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="38a5a-112">Ez a parancs a tárolóval regisztrált összes biztonságimásolat-kezelő kiszolgálót beveszi.</span><span class="sxs-lookup"><span data-stu-id="38a5a-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="38a5a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38a5a-113">PARAMETERS</span></span>

### <span data-ttu-id="38a5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a5a-114">-DefaultProfile</span></span>
<span data-ttu-id="38a5a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38a5a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38a5a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="38a5a-116">-Name</span></span>
<span data-ttu-id="38a5a-117">A lekért biztonsági másolat-kezelő kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38a5a-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="38a5a-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="38a5a-118">-VaultId</span></span>
<span data-ttu-id="38a5a-119">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38a5a-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="38a5a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a5a-120">CommonParameters</span></span>
<span data-ttu-id="38a5a-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a5a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a5a-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38a5a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a5a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38a5a-123">INPUTS</span></span>

### <span data-ttu-id="38a5a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="38a5a-124">System.String</span></span>

## <span data-ttu-id="38a5a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38a5a-125">OUTPUTS</span></span>

### <span data-ttu-id="38a5a-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="38a5a-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="38a5a-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38a5a-127">NOTES</span></span>

## <span data-ttu-id="38a5a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38a5a-128">RELATED LINKS</span></span>

[<span data-ttu-id="38a5a-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="38a5a-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


