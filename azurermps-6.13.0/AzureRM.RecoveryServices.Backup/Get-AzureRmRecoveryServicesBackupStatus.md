---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679525"
---
# <span data-ttu-id="2a631-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="2a631-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="2a631-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a631-102">SYNOPSIS</span></span>
<span data-ttu-id="2a631-103">Annak vizsgálata, hogy a kar erőforrása biztonsági másolatot készített-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="2a631-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a631-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a631-104">SYNTAX</span></span>

### <span data-ttu-id="2a631-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a631-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a631-106">Azonosító</span><span class="sxs-lookup"><span data-stu-id="2a631-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a631-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a631-107">DESCRIPTION</span></span>
<span data-ttu-id="2a631-108">A parancs a null/EMPTY értéket adja eredményül, ha a megadott erőforrás nem védett az előfizetéshez tartozó helyreállítási szolgáltatások boltozata alatt.</span><span class="sxs-lookup"><span data-stu-id="2a631-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="2a631-109">Ha meg van védve, a megfelelő Vault-részleteket a program visszaadja.</span><span class="sxs-lookup"><span data-stu-id="2a631-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="2a631-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2a631-110">EXAMPLES</span></span>

### <span data-ttu-id="2a631-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2a631-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="2a631-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a631-112">PARAMETERS</span></span>

### <span data-ttu-id="2a631-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a631-113">-DefaultProfile</span></span>
<span data-ttu-id="2a631-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a631-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a631-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a631-115">-Name</span></span>
<span data-ttu-id="2a631-116">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="2a631-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

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

### <span data-ttu-id="2a631-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a631-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a631-118">Annak az Azure-erőforrásnak az erőforráscsoport nevét adja meg, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-boltozat már védett.</span><span class="sxs-lookup"><span data-stu-id="2a631-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="2a631-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a631-119">-ResourceId</span></span>
<span data-ttu-id="2a631-120">Annak az Azure-erőforrásnak az AZONOSÍTÓját, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy RecoveryServices-tároló már védett.</span><span class="sxs-lookup"><span data-stu-id="2a631-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a631-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="2a631-121">-Type</span></span>
<span data-ttu-id="2a631-122">Annak az Azure-erőforrásnak a neve, amelynek a reprezentatív elemét ellenőrizni kell, ha az előfizetésben egy helyreállítási szolgáltatások boltozata már védett.</span><span class="sxs-lookup"><span data-stu-id="2a631-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a631-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a631-123">CommonParameters</span></span>
<span data-ttu-id="2a631-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a631-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a631-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a631-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a631-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a631-126">INPUTS</span></span>

### <span data-ttu-id="2a631-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2a631-127">System.String</span></span>

## <span data-ttu-id="2a631-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a631-128">OUTPUTS</span></span>

### <span data-ttu-id="2a631-129">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="2a631-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="2a631-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a631-130">NOTES</span></span>

## <span data-ttu-id="2a631-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a631-131">RELATED LINKS</span></span>
