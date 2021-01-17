---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: cc52435ff0b288656e4a917620659737f33916ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467239"
---
# <span data-ttu-id="553d6-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="553d6-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="553d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="553d6-102">SYNOPSIS</span></span>
<span data-ttu-id="553d6-103">A SCDPM-kiszolgáló vagy a biztonsági másolat-kiszolgáló regisztrációjának visszaállítása a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="553d6-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="553d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="553d6-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="553d6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="553d6-105">DESCRIPTION</span></span>
<span data-ttu-id="553d6-106">A **Unregister-AzRecoveryServicesBackupManagementServer** parancsmag nem regisztrálja a System Center Data Protection Manager (SCDPM) kiszolgálót vagy egy Azure Backup-kiszolgálót a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="553d6-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="553d6-107">Ez a parancsmag eltávolítja a tárolóból nem regisztrált kiszolgálókra mutató hivatkozásokat.</span><span class="sxs-lookup"><span data-stu-id="553d6-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="553d6-108">Mielőtt törölné egy tároló regisztrációját, törölnie kell a tárolóhoz társított védett adatokat.</span><span class="sxs-lookup"><span data-stu-id="553d6-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="553d6-109">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="553d6-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="553d6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="553d6-110">EXAMPLES</span></span>

### <span data-ttu-id="553d6-111">1. példa: SCDPM-kiszolgáló regisztrációjának visszaszava a tárolóból</span><span class="sxs-lookup"><span data-stu-id="553d6-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```powershell
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="553d6-112">Az első parancs lekérte a dpmserver01.contoso.com nevű biztonságimásolat-kezelő kiszolgálót, majd tárolja azt a $BMS változóban.</span><span class="sxs-lookup"><span data-stu-id="553d6-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="553d6-113">A második parancs nem regisztrálja a SCDPM-kiszolgálót a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="553d6-113">The second command unregisters the SCDPM server from the vault.</span></span>

### <span data-ttu-id="553d6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="553d6-114">Example 2</span></span>

<span data-ttu-id="553d6-115">A SCDPM-kiszolgáló vagy a biztonsági másolat-kiszolgáló regisztrációjának visszaállítása a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="553d6-115">Unregisters a SCDPM server or Backup server from the vault.</span></span> <span data-ttu-id="553d6-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="553d6-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer <BackupEngineBase> -VaultId $vault.ID
```

## <span data-ttu-id="553d6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="553d6-117">PARAMETERS</span></span>

### <span data-ttu-id="553d6-118">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="553d6-118">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="553d6-119">A helyreállítási szolgáltatások biztonsági mentési tárolója.</span><span class="sxs-lookup"><span data-stu-id="553d6-119">The recovery services backup container.</span></span>

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

### <span data-ttu-id="553d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553d6-120">-DefaultProfile</span></span>
<span data-ttu-id="553d6-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="553d6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="553d6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="553d6-122">-PassThru</span></span>
<span data-ttu-id="553d6-123">Adja vissza a biztonsági másolat-kezelő kiszolgálót a törléshez.</span><span class="sxs-lookup"><span data-stu-id="553d6-123">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="553d6-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="553d6-124">-VaultId</span></span>
<span data-ttu-id="553d6-125">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="553d6-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="553d6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="553d6-126">-Confirm</span></span>
<span data-ttu-id="553d6-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="553d6-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553d6-128">-WhatIf</span></span>
<span data-ttu-id="553d6-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="553d6-129">Shows what would happen if the cmdlet runs.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553d6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553d6-130">CommonParameters</span></span>
<span data-ttu-id="553d6-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553d6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553d6-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="553d6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553d6-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="553d6-133">INPUTS</span></span>

### <span data-ttu-id="553d6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="553d6-134">System.String</span></span>

## <span data-ttu-id="553d6-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="553d6-135">OUTPUTS</span></span>

### <span data-ttu-id="553d6-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="553d6-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="553d6-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="553d6-137">NOTES</span></span>

## <span data-ttu-id="553d6-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="553d6-138">RELATED LINKS</span></span>

[<span data-ttu-id="553d6-139">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="553d6-139">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


