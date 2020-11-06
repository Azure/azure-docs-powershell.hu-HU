---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492234"
---
# <span data-ttu-id="7c98c-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="7c98c-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="7c98c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c98c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c98c-103">Létrehoz egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához.</span><span class="sxs-lookup"><span data-stu-id="7c98c-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c98c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c98c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c98c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c98c-105">DESCRIPTION</span></span>
<span data-ttu-id="7c98c-106">Létrehoz egy olyan lemezkezelő-objektumot, amely egy Azure Virtual Machine-merevlemezt rendel a gyorsítótár-tároló fiókhoz és a TARGET Storage (helyreállítási régió) fiókhoz, amelyet a lemez replikálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="7c98c-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="7c98c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c98c-107">EXAMPLES</span></span>

### <span data-ttu-id="7c98c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c98c-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="7c98c-109">Létrehozhat egy lemezkezelő-objektumot az Azure Virtual Machine-lemezek replikálásához. Az Azure-ban az Azure EnableD és a ReProTect műveletben használatos.</span><span class="sxs-lookup"><span data-stu-id="7c98c-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="7c98c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c98c-110">PARAMETERS</span></span>

### <span data-ttu-id="7c98c-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c98c-111">-Confirm</span></span>
<span data-ttu-id="7c98c-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c98c-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c98c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c98c-113">-DefaultProfile</span></span>
<span data-ttu-id="7c98c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c98c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c98c-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7c98c-115">-LogStorageAccountId</span></span>
<span data-ttu-id="7c98c-116">A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c98c-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c98c-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7c98c-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7c98c-118">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c98c-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c98c-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="7c98c-119">-VhdUri</span></span>
<span data-ttu-id="7c98c-120">Adja meg annak a lemeznek a VHD-URI-jét, amelyre a megfeleltetés megfelel.</span><span class="sxs-lookup"><span data-stu-id="7c98c-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c98c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c98c-121">-WhatIf</span></span>
<span data-ttu-id="7c98c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c98c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c98c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c98c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c98c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c98c-124">CommonParameters</span></span>
<span data-ttu-id="7c98c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c98c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c98c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c98c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c98c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c98c-127">INPUTS</span></span>

### <span data-ttu-id="7c98c-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c98c-128">None</span></span>

## <span data-ttu-id="7c98c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c98c-129">OUTPUTS</span></span>

### <span data-ttu-id="7c98c-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="7c98c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="7c98c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c98c-131">NOTES</span></span>

## <span data-ttu-id="7c98c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c98c-132">RELATED LINKS</span></span>
