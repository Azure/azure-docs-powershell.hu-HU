---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503071"
---
# <span data-ttu-id="c6733-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="c6733-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="c6733-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6733-102">SYNOPSIS</span></span>
<span data-ttu-id="c6733-103">A megadott készlet operációs rendszerhez tartozó verziójának módosítása.</span><span class="sxs-lookup"><span data-stu-id="c6733-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6733-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6733-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6733-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6733-105">DESCRIPTION</span></span>
<span data-ttu-id="c6733-106">A **set-AzureBatchPoolOSVersion** parancsmag a megadott készlet operációs rendszerének verziószámát módosítja.</span><span class="sxs-lookup"><span data-stu-id="c6733-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="c6733-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6733-107">EXAMPLES</span></span>

### <span data-ttu-id="c6733-108">1. példa: a cél operációs rendszer verziójának beállítása</span><span class="sxs-lookup"><span data-stu-id="c6733-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="c6733-109">Ez a parancs a MyPool alkalmazáskészlet operációs rendszerének verziószámát a WA-GUEST-OS-4.20 _201505-01 értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="c6733-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="c6733-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6733-110">PARAMETERS</span></span>

### <span data-ttu-id="c6733-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c6733-111">-BatchContext</span></span>
<span data-ttu-id="c6733-112">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="c6733-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c6733-113">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="c6733-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c6733-114">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="c6733-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c6733-115">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="c6733-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c6733-116">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="c6733-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6733-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6733-117">-DefaultProfile</span></span>
<span data-ttu-id="c6733-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6733-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6733-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="c6733-119">-Id</span></span>
<span data-ttu-id="c6733-120">A készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6733-120">Specifies the ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6733-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="c6733-121">-TargetOSVersion</span></span>
<span data-ttu-id="c6733-122">Az Azure Guest Operating System verziószámát adja meg a készletben lévő virtuális gépeken való telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="c6733-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="c6733-123">Az Azure vendég operációs rendszer verzióiról további információt az Azure Guest Operating OS kiadásai és az SDK kompatibilitási mátrixa (című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="c6733-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6733-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6733-124">CommonParameters</span></span>
<span data-ttu-id="c6733-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6733-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6733-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6733-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6733-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6733-127">INPUTS</span></span>

### <span data-ttu-id="c6733-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c6733-128">BatchAccountContext</span></span>
<span data-ttu-id="c6733-129">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c6733-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c6733-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="c6733-130">String</span></span>
<span data-ttu-id="c6733-131">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="c6733-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c6733-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6733-132">OUTPUTS</span></span>

## <span data-ttu-id="c6733-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6733-133">NOTES</span></span>

## <span data-ttu-id="c6733-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6733-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6733-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c6733-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


