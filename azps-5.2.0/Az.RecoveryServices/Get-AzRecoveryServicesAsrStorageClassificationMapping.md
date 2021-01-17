---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352565"
---
# <span data-ttu-id="b39f9-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b39f9-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="b39f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b39f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b39f9-103">AsR-tárolóbesorolási megfeleltetéseket kap.</span><span class="sxs-lookup"><span data-stu-id="b39f9-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="b39f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b39f9-104">SYNTAX</span></span>

### <span data-ttu-id="b39f9-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b39f9-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b39f9-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b39f9-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b39f9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b39f9-107">DESCRIPTION</span></span>
<span data-ttu-id="b39f9-108">A **Get-AzRecoveryServicesAsrStorageClassificationMapping** parancsmag begyűjte az ASR-tárbesorolás megfeleltetésének részleteit.</span><span class="sxs-lookup"><span data-stu-id="b39f9-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="b39f9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b39f9-109">EXAMPLES</span></span>

### <span data-ttu-id="b39f9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b39f9-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="b39f9-111">List all storage classification mappings corresponding to the specified storage classification.</span><span class="sxs-lookup"><span data-stu-id="b39f9-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="b39f9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b39f9-112">PARAMETERS</span></span>

### <span data-ttu-id="b39f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39f9-113">-DefaultProfile</span></span>
<span data-ttu-id="b39f9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b39f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b39f9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b39f9-115">-Name</span></span>
<span data-ttu-id="b39f9-116">A lekért tárbesorolási megfeleltetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b39f9-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b39f9-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="b39f9-117">-StorageClassification</span></span>
<span data-ttu-id="b39f9-118">Asr storage classification objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="b39f9-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="b39f9-119">A parancsmag ASR-tárolóbesorolási megfeleltetéseket kap a megadott tárolási besorolásnak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b39f9-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b39f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39f9-120">CommonParameters</span></span>
<span data-ttu-id="b39f9-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b39f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39f9-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b39f9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39f9-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b39f9-123">INPUTS</span></span>

### <span data-ttu-id="b39f9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="b39f9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="b39f9-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b39f9-125">OUTPUTS</span></span>

### <span data-ttu-id="b39f9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b39f9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="b39f9-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b39f9-127">NOTES</span></span>

## <span data-ttu-id="b39f9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b39f9-128">RELATED LINKS</span></span>

[<span data-ttu-id="b39f9-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b39f9-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="b39f9-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b39f9-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
