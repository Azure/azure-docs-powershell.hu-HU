---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: cd3e3e2ad33cb01935a2594571145f0667c9a3e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669684"
---
# <span data-ttu-id="03786-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="03786-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="03786-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03786-102">SYNOPSIS</span></span>
<span data-ttu-id="03786-103">Annak vizsgálata, hogy a kar erőforrása biztonsági másolatot készített-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="03786-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="03786-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03786-104">SYNTAX</span></span>

### <span data-ttu-id="03786-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03786-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03786-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="03786-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03786-107">Azonosító</span><span class="sxs-lookup"><span data-stu-id="03786-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03786-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="03786-108">DESCRIPTION</span></span>
<span data-ttu-id="03786-109">A parancs a null/EMPTY értéket adja eredményül, ha a megadott erőforrás nem védett az előfizetéshez tartozó helyreállítási szolgáltatások boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="03786-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="03786-110">Ha meg van védve, a megfelelő Vault-részleteket a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="03786-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="03786-111">Példák</span><span class="sxs-lookup"><span data-stu-id="03786-111">EXAMPLES</span></span>

### <span data-ttu-id="03786-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03786-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="03786-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03786-113">PARAMETERS</span></span>

### <span data-ttu-id="03786-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03786-114">-DefaultProfile</span></span>
<span data-ttu-id="03786-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03786-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03786-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03786-116">-Name</span></span>
<span data-ttu-id="03786-117">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="03786-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03786-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="03786-118">-ProtectableObjectName</span></span>
<span data-ttu-id="03786-119">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="03786-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03786-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03786-120">-ResourceGroupName</span></span>
<span data-ttu-id="03786-121">Annak az Azure-erőforrásnak az erőforráscsoport nevét adja meg, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-boltozat már védett.</span><span class="sxs-lookup"><span data-stu-id="03786-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03786-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03786-122">-ResourceId</span></span>
<span data-ttu-id="03786-123">Annak az Azure-erőforrásnak az AZONOSÍTÓját, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-tároló már védett.</span><span class="sxs-lookup"><span data-stu-id="03786-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03786-124">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="03786-124">-Type</span></span>
<span data-ttu-id="03786-125">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="03786-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03786-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03786-126">CommonParameters</span></span>
<span data-ttu-id="03786-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03786-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03786-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03786-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03786-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03786-129">INPUTS</span></span>

### <span data-ttu-id="03786-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03786-130">System.String</span></span>

## <span data-ttu-id="03786-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03786-131">OUTPUTS</span></span>

### <span data-ttu-id="03786-132">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="03786-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="03786-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03786-133">NOTES</span></span>

## <span data-ttu-id="03786-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03786-134">RELATED LINKS</span></span>
