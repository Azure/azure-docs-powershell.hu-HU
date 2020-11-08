---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 1e10fe2aa534e236c99468ec672e6a0eeadae469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014719"
---
# <span data-ttu-id="2c5ff-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="2c5ff-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="2c5ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5ff-103">Annak vizsgálata, hogy a kar erőforrása biztonsági másolatot készített-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="2c5ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c5ff-104">SYNTAX</span></span>

### <span data-ttu-id="2c5ff-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c5ff-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c5ff-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="2c5ff-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c5ff-107">Azonosító</span><span class="sxs-lookup"><span data-stu-id="2c5ff-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c5ff-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c5ff-108">DESCRIPTION</span></span>
<span data-ttu-id="2c5ff-109">A parancs a null/EMPTY értéket adja eredményül, ha a megadott erőforrás nem védett az előfizetéshez tartozó helyreállítási szolgáltatások boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="2c5ff-110">Ha meg van védve, a megfelelő Vault-részleteket a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="2c5ff-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2c5ff-111">EXAMPLES</span></span>

### <span data-ttu-id="2c5ff-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2c5ff-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="2c5ff-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c5ff-113">PARAMETERS</span></span>

### <span data-ttu-id="2c5ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5ff-114">-DefaultProfile</span></span>
<span data-ttu-id="2c5ff-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c5ff-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c5ff-116">-Name</span></span>
<span data-ttu-id="2c5ff-117">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="2c5ff-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="2c5ff-118">-ProtectableObjectName</span></span>
<span data-ttu-id="2c5ff-119">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="2c5ff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5ff-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c5ff-121">Annak az Azure-erőforrásnak az erőforráscsoport nevét adja meg, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-boltozat már védett.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="2c5ff-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c5ff-122">-ResourceId</span></span>
<span data-ttu-id="2c5ff-123">Annak az Azure-erőforrásnak az AZONOSÍTÓját, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-tároló már védett.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="2c5ff-124">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="2c5ff-124">-Type</span></span>
<span data-ttu-id="2c5ff-125">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="2c5ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5ff-126">CommonParameters</span></span>
<span data-ttu-id="2c5ff-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c5ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5ff-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c5ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5ff-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c5ff-129">INPUTS</span></span>

### <span data-ttu-id="2c5ff-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2c5ff-130">System.String</span></span>

## <span data-ttu-id="2c5ff-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c5ff-131">OUTPUTS</span></span>

### <span data-ttu-id="2c5ff-132">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="2c5ff-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="2c5ff-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c5ff-133">NOTES</span></span>

## <span data-ttu-id="2c5ff-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c5ff-134">RELATED LINKS</span></span>
