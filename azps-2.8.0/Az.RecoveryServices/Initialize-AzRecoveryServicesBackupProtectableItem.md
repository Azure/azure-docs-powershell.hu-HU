---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838561"
---
# <span data-ttu-id="51d64-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="51d64-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="51d64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51d64-102">SYNOPSIS</span></span>
<span data-ttu-id="51d64-103">Ez a parancs elindítja az adott tárolóban lévő adott terhelési típus védtelen elemeinek felderítését.</span><span class="sxs-lookup"><span data-stu-id="51d64-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="51d64-104">Ha az adatbázis-alkalmazás nem az automatikus védelemmel van ellátva, használja ezt a parancsot az új DBs-t a hozzáadásuk után, és folytassa a védelmet.</span><span class="sxs-lookup"><span data-stu-id="51d64-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="51d64-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51d64-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51d64-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="51d64-106">DESCRIPTION</span></span>
<span data-ttu-id="51d64-107">a parancsmag a tárolón belüli bizonyos terhelésekre vonatkozó kérdésekkel kapcsolatos kérdésekről szól.</span><span class="sxs-lookup"><span data-stu-id="51d64-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="51d64-108">Ezzel olyan műveletet indít el, amely védett elemeket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="51d64-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="51d64-109">Példák</span><span class="sxs-lookup"><span data-stu-id="51d64-109">EXAMPLES</span></span>

### <span data-ttu-id="51d64-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51d64-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="51d64-111">A parancsmag az új védett elemek felderítési műveletét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="51d64-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="51d64-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51d64-112">PARAMETERS</span></span>

### <span data-ttu-id="51d64-113">-Container</span><span class="sxs-lookup"><span data-stu-id="51d64-113">-Container</span></span>
<span data-ttu-id="51d64-114">Tároló, ahol az elem található</span><span class="sxs-lookup"><span data-stu-id="51d64-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51d64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d64-115">-DefaultProfile</span></span>
<span data-ttu-id="51d64-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51d64-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51d64-117">-VaultId</span><span class="sxs-lookup"><span data-stu-id="51d64-117">-VaultId</span></span>
<span data-ttu-id="51d64-118">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="51d64-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="51d64-119">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="51d64-119">-WorkloadType</span></span>
<span data-ttu-id="51d64-120">Az erőforrás terhelési típusa (például: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="51d64-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d64-121">CommonParameters</span></span>
<span data-ttu-id="51d64-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51d64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d64-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d64-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51d64-124">INPUTS</span></span>

### <span data-ttu-id="51d64-125">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="51d64-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="51d64-126">System. String</span><span class="sxs-lookup"><span data-stu-id="51d64-126">System.String</span></span>

## <span data-ttu-id="51d64-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51d64-127">OUTPUTS</span></span>

### <span data-ttu-id="51d64-128">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="51d64-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="51d64-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51d64-129">NOTES</span></span>

## <span data-ttu-id="51d64-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51d64-130">RELATED LINKS</span></span>