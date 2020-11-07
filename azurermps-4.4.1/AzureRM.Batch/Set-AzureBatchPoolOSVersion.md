---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679116"
---
# <span data-ttu-id="adc88-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="adc88-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="adc88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adc88-102">SYNOPSIS</span></span>
<span data-ttu-id="adc88-103">A megadott készlet operációs rendszerhez tartozó verziójának módosítása.</span><span class="sxs-lookup"><span data-stu-id="adc88-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adc88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adc88-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc88-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="adc88-105">DESCRIPTION</span></span>
<span data-ttu-id="adc88-106">A **set-AzureBatchPoolOSVersion** parancsmag a megadott készlet operációs rendszerének verziószámát módosítja.</span><span class="sxs-lookup"><span data-stu-id="adc88-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="adc88-107">Példák</span><span class="sxs-lookup"><span data-stu-id="adc88-107">EXAMPLES</span></span>

### <span data-ttu-id="adc88-108">1. példa: a cél operációs rendszer verziójának beállítása</span><span class="sxs-lookup"><span data-stu-id="adc88-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="adc88-109">Ez a parancs a MyPool alkalmazáskészlet operációs rendszerének verziószámát a WA-GUEST-OS-4.20 _201505-01 értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="adc88-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="adc88-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adc88-110">PARAMETERS</span></span>

### <span data-ttu-id="adc88-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="adc88-111">-BatchContext</span></span>
<span data-ttu-id="adc88-112">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="adc88-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="adc88-113">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="adc88-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="adc88-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="adc88-114">-Id</span></span>
<span data-ttu-id="adc88-115">A készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="adc88-115">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="adc88-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="adc88-116">-TargetOSVersion</span></span>
<span data-ttu-id="adc88-117">Az Azure Guest Operating System verziószámát adja meg a készletben lévő virtuális gépeken való telepítéshez.</span><span class="sxs-lookup"><span data-stu-id="adc88-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="adc88-118">Az Azure vendég operációs rendszer verzióiról további információt az Azure Guest Operating OS kiadásai és az SDK kompatibilitási mátrixa (című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="adc88-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="adc88-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc88-119">-DefaultProfile</span></span>
<span data-ttu-id="adc88-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adc88-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adc88-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc88-121">CommonParameters</span></span>
<span data-ttu-id="adc88-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adc88-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc88-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc88-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc88-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adc88-124">INPUTS</span></span>

### <span data-ttu-id="adc88-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="adc88-125">BatchAccountContext</span></span>
<span data-ttu-id="adc88-126">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="adc88-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="adc88-127">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="adc88-127">String</span></span>
<span data-ttu-id="adc88-128">Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="adc88-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="adc88-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adc88-129">OUTPUTS</span></span>

## <span data-ttu-id="adc88-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adc88-130">NOTES</span></span>

## <span data-ttu-id="adc88-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adc88-131">RELATED LINKS</span></span>

[<span data-ttu-id="adc88-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="adc88-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


