---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501691"
---
# <span data-ttu-id="12266-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="12266-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="12266-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12266-102">SYNOPSIS</span></span>
<span data-ttu-id="12266-103">A SCDPM-kiszolgáló vagy a biztonsági másolat kiszolgálójának törlése a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="12266-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12266-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12266-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12266-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12266-105">DESCRIPTION</span></span>
<span data-ttu-id="12266-106">A **unregister-AzureRmRecoveryServicesBackupManagementServer** parancsmag a System Center Data Protection Manager (SCDPM) kiszolgálóját vagy az Azure Backup Servert a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="12266-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="12266-107">Ez a parancsmag eltávolítja azokat a kiszolgálókat, amelyek nem lettek rögzítve a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="12266-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="12266-108">A tároló törlése előtt törölnie kell az adott tárolóhoz társított összes védett adatot.</span><span class="sxs-lookup"><span data-stu-id="12266-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="12266-109">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="12266-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="12266-110">Példák</span><span class="sxs-lookup"><span data-stu-id="12266-110">EXAMPLES</span></span>

### <span data-ttu-id="12266-111">1. példa: SCDPM-kiszolgáló regisztrációjának megszüntetése a boltozatról</span><span class="sxs-lookup"><span data-stu-id="12266-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="12266-112">Az első parancs a dpmserver01.contoso.com nevű Backup Management Servert kapja, majd a $BMS változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="12266-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="12266-113">A második parancs a SCDPM-kiszolgáló regisztrációját a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="12266-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="12266-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12266-114">PARAMETERS</span></span>

### <span data-ttu-id="12266-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="12266-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="12266-116">Itt adhatja meg a SCDPM-kiszolgáló objektumát a regisztráció törléséhez.</span><span class="sxs-lookup"><span data-stu-id="12266-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="12266-117">**BackupManagementServer** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupManagementServer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="12266-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12266-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12266-118">-DefaultProfile</span></span>
<span data-ttu-id="12266-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12266-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12266-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12266-120">CommonParameters</span></span>
<span data-ttu-id="12266-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12266-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12266-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12266-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12266-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12266-123">INPUTS</span></span>

## <span data-ttu-id="12266-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12266-124">OUTPUTS</span></span>

## <span data-ttu-id="12266-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12266-125">NOTES</span></span>

## <span data-ttu-id="12266-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12266-126">RELATED LINKS</span></span>

[<span data-ttu-id="12266-127">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="12266-127">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


