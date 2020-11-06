---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: e3e4858e3cb4f3c54c502ac14fb2c5d8e3ba0c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492020"
---
# <span data-ttu-id="f29a6-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f29a6-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="f29a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f29a6-102">SYNOPSIS</span></span>
<span data-ttu-id="f29a6-103">Biztonságimásolat-házirendek biztonsági mentése a biztonsági mentéshez.</span><span class="sxs-lookup"><span data-stu-id="f29a6-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f29a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f29a6-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f29a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f29a6-105">DESCRIPTION</span></span>
<span data-ttu-id="f29a6-106">A **Get-AzureRmBackupProtectionPolicy** parancsmag biztonsági házirendeket kap az Azure Backup-Vault-hoz.</span><span class="sxs-lookup"><span data-stu-id="f29a6-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="f29a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f29a6-107">EXAMPLES</span></span>

### <span data-ttu-id="f29a6-108">Példa 1: a házirendek megtekintése a boltozatban</span><span class="sxs-lookup"><span data-stu-id="f29a6-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="f29a6-109">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="f29a6-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="f29a6-110">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f29a6-110">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="f29a6-111">A második parancs beolvassa az összes biztonsági mentési házirendet az $Vault boltozatához.</span><span class="sxs-lookup"><span data-stu-id="f29a6-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="f29a6-112">2. példa: meghatározott házirend beolvasása egy boltozatból</span><span class="sxs-lookup"><span data-stu-id="f29a6-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="f29a6-113">Az első parancs a Vault03 nevű boltozatot a **Get-AzureRmBackupVault** parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="f29a6-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="f29a6-114">A parancs az objektumot a $Vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f29a6-114">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="f29a6-115">A második parancs beolvassa a DefaultPolicy nevű biztonsági házirendet a $Vault boltozatához.</span><span class="sxs-lookup"><span data-stu-id="f29a6-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="f29a6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f29a6-116">PARAMETERS</span></span>

### <span data-ttu-id="f29a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29a6-117">-DefaultProfile</span></span>
<span data-ttu-id="f29a6-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f29a6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f29a6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f29a6-119">-Name</span></span>
<span data-ttu-id="f29a6-120">Annak a házirendnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="f29a6-120">Specifies the name of the policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f29a6-121">-Boltozat</span><span class="sxs-lookup"><span data-stu-id="f29a6-121">-Vault</span></span>
<span data-ttu-id="f29a6-122">Annak a biztonságimásolat-tárolónak a megadása, amelyhez ez a parancsmag házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="f29a6-122">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="f29a6-123">**AzureRmBackupVault** objektum beolvasásához használja az Get-AzureRmBackupVault parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f29a6-123">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="f29a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29a6-124">CommonParameters</span></span>
<span data-ttu-id="f29a6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f29a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29a6-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f29a6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29a6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f29a6-127">INPUTS</span></span>

### <span data-ttu-id="f29a6-128">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="f29a6-128">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="f29a6-129">Paraméterek: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f29a6-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="f29a6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f29a6-130">OUTPUTS</span></span>

### <span data-ttu-id="f29a6-131">Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f29a6-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="f29a6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f29a6-132">NOTES</span></span>

## <span data-ttu-id="f29a6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f29a6-133">RELATED LINKS</span></span>

[<span data-ttu-id="f29a6-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f29a6-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="f29a6-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f29a6-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="f29a6-136">Új – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f29a6-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="f29a6-137">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f29a6-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)


