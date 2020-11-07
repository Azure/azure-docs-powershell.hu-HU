---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 7bca28da7b4729a414fafc5268bc4e0e02ee3c72
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843057"
---
# <span data-ttu-id="adabc-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="adabc-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="adabc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adabc-102">SYNOPSIS</span></span>
<span data-ttu-id="adabc-103">Az Azure Storage szolgáltatás metrikájának tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="adabc-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="adabc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adabc-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adabc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="adabc-105">DESCRIPTION</span></span>
<span data-ttu-id="adabc-106">A **Get-AzStorageServiceMetricsProperty** parancsmag metrikák tulajdonságait az Azure Storage szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="adabc-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="adabc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="adabc-107">EXAMPLES</span></span>

### <span data-ttu-id="adabc-108">1. példa: a blob-szolgáltatás metrikák tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="adabc-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="adabc-109">Ennek a parancsnak a metrikák típusa esetén a blob-tárolóra vonatkozó tulajdonságokat kell kinéznie.</span><span class="sxs-lookup"><span data-stu-id="adabc-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="adabc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adabc-110">PARAMETERS</span></span>

### <span data-ttu-id="adabc-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="adabc-111">-Context</span></span>
<span data-ttu-id="adabc-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="adabc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="adabc-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="adabc-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adabc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adabc-114">-DefaultProfile</span></span>
<span data-ttu-id="adabc-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adabc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adabc-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="adabc-116">-MetricsType</span></span>
<span data-ttu-id="adabc-117">A mérőszám típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="adabc-117">Specifies a metrics type.</span></span>
<span data-ttu-id="adabc-118">Ez a parancsmag az Azure Storage Service metrikájának tulajdonságait adja meg a mérőszámok típusához, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="adabc-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="adabc-119">A paraméter elfogadható értékei a következők: óra és perc.</span><span class="sxs-lookup"><span data-stu-id="adabc-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adabc-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="adabc-120">-ServiceType</span></span>
<span data-ttu-id="adabc-121">A tárterület szolgáltatás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="adabc-121">Specifies the storage service type.</span></span>
<span data-ttu-id="adabc-122">Ez a parancsmag a paraméter által megadott típus metrikájának tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="adabc-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="adabc-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="adabc-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="adabc-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="adabc-124">Blob</span></span> 
- <span data-ttu-id="adabc-125">Táblázat</span><span class="sxs-lookup"><span data-stu-id="adabc-125">Table</span></span>
- <span data-ttu-id="adabc-126">Várólista</span><span class="sxs-lookup"><span data-stu-id="adabc-126">Queue</span></span>
- <span data-ttu-id="adabc-127">Fájl: a fájl értéke jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="adabc-127">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adabc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adabc-128">CommonParameters</span></span>
<span data-ttu-id="adabc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adabc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adabc-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adabc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adabc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adabc-131">INPUTS</span></span>

### <span data-ttu-id="adabc-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="adabc-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="adabc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adabc-133">OUTPUTS</span></span>

### <span data-ttu-id="adabc-134">Microsoft. WindowsAz. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="adabc-134">Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="adabc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adabc-135">NOTES</span></span>

## <span data-ttu-id="adabc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adabc-136">RELATED LINKS</span></span>

[<span data-ttu-id="adabc-137">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="adabc-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="adabc-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="adabc-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


