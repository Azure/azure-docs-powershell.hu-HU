---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: d85e0ca61b86e523c6d73ea8d2349d7d692aafb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501199"
---
# <span data-ttu-id="87a9b-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="87a9b-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="87a9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="87a9b-103">A megadott készlet operációs rendszerhez tartozó verziójának módosítása.</span><span class="sxs-lookup"><span data-stu-id="87a9b-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87a9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87a9b-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87a9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="87a9b-106">A **set-AzureBatchPoolOSVersion** parancsmag a megadott készlet operációs rendszerének verziószámát módosítja.</span><span class="sxs-lookup"><span data-stu-id="87a9b-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="87a9b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87a9b-107">EXAMPLES</span></span>

### <span data-ttu-id="87a9b-108">1. példa: a cél operációs rendszer verziójának beállítása</span><span class="sxs-lookup"><span data-stu-id="87a9b-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="87a9b-109">Ez a parancs a MyPool alkalmazáskészlet operációs rendszerének verziószámát a WA-GUEST-OS-4.20 _201505-01 értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="87a9b-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="87a9b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87a9b-110">PARAMETERS</span></span>

### <span data-ttu-id="87a9b-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="87a9b-111">-BatchContext</span></span>
<span data-ttu-id="87a9b-112">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="87a9b-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="87a9b-113">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="87a9b-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="87a9b-114">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="87a9b-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="87a9b-115">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="87a9b-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="87a9b-116">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="87a9b-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87a9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a9b-117">-DefaultProfile</span></span>
<span data-ttu-id="87a9b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87a9b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87a9b-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="87a9b-119">-Id</span></span>
<span data-ttu-id="87a9b-120">A készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="87a9b-120">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87a9b-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="87a9b-121">-TargetOSVersion</span></span>
<span data-ttu-id="87a9b-122">Az Azure Guest Operating System verziószámát adja meg a készletben lévő virtuális gépeken való telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="87a9b-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="87a9b-123">Az Azure vendég operációs rendszer verzióiról további információt az Azure Guest Operating OS kiadásai és az SDK kompatibilitási mátrixa (című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="87a9b-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a9b-124">CommonParameters</span></span>
<span data-ttu-id="87a9b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87a9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a9b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a9b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a9b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87a9b-127">INPUTS</span></span>

### <span data-ttu-id="87a9b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="87a9b-128">System.String</span></span>

### <span data-ttu-id="87a9b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="87a9b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="87a9b-130">Paraméterek: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87a9b-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="87a9b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87a9b-131">OUTPUTS</span></span>

### <span data-ttu-id="87a9b-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="87a9b-132">System.Void</span></span>

## <span data-ttu-id="87a9b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87a9b-133">NOTES</span></span>

## <span data-ttu-id="87a9b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87a9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="87a9b-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="87a9b-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


