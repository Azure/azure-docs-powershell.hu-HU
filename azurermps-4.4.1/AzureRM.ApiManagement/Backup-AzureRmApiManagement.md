---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d036b31f521736420b91b04b4f6f5513f3dbc50d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500983"
---
# <span data-ttu-id="ee061-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee061-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="ee061-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee061-102">SYNOPSIS</span></span>
<span data-ttu-id="ee061-103">Biztonsági másolatot készíthet egy API-kezelési szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="ee061-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee061-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee061-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee061-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee061-105">DESCRIPTION</span></span>
<span data-ttu-id="ee061-106">A **Backup-AzureRmApiManagement** parancsmag egy Azure API-kezelési szolgáltatás példányát támogatja.</span><span class="sxs-lookup"><span data-stu-id="ee061-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="ee061-107">Ez a parancsmag az Azure Storage blob néven tárolja a biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="ee061-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="ee061-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ee061-108">EXAMPLES</span></span>

### <span data-ttu-id="ee061-109">1. példa: API-kezelési szolgáltatás biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="ee061-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="ee061-110">Ezzel a paranccsal biztonsági másolatot készíthet egy API-kezelési szolgáltatásról a tárolási blobra.</span><span class="sxs-lookup"><span data-stu-id="ee061-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="ee061-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee061-111">PARAMETERS</span></span>

### <span data-ttu-id="ee061-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee061-112">-Name</span></span>
<span data-ttu-id="ee061-113">Itt adhatja meg az API-kezelés telepített példányának a nevét, amelyre a parancsmag biztonsági másolat készül.</span><span class="sxs-lookup"><span data-stu-id="ee061-113">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee061-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee061-114">-PassThru</span></span>
<span data-ttu-id="ee061-115">Azt jelzi, hogy ez a parancsmag a biztonsági másolat **PsApiManagement** objektumát adja vissza, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="ee061-115">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee061-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee061-116">-ResourceGroupName</span></span>
<span data-ttu-id="ee061-117">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="ee061-117">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee061-118">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ee061-118">-StorageContext</span></span>
<span data-ttu-id="ee061-119">A tárterület-kapcsolat kontextusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee061-119">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee061-120">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="ee061-120">-TargetBlobName</span></span>
<span data-ttu-id="ee061-121">A biztonsági másolat blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee061-121">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="ee061-122">Ha a blob nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ee061-122">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="ee061-123">Ez a parancsmag a következő minta alapján hoz létre alapértelmezett értéket:</span><span class="sxs-lookup"><span data-stu-id="ee061-123">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="ee061-124">{Name}-{ÉÉÉÉ-HH-NN-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="ee061-124">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee061-125">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="ee061-125">-TargetContainerName</span></span>
<span data-ttu-id="ee061-126">A biztonsági másolat blob-tárolójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee061-126">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="ee061-127">Ha a tároló nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ee061-127">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee061-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee061-128">-DefaultProfile</span></span>
<span data-ttu-id="ee061-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee061-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee061-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee061-130">CommonParameters</span></span>
<span data-ttu-id="ee061-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee061-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee061-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee061-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee061-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee061-133">INPUTS</span></span>

## <span data-ttu-id="ee061-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee061-134">OUTPUTS</span></span>

### <span data-ttu-id="ee061-135">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee061-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ee061-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee061-136">NOTES</span></span>

## <span data-ttu-id="ee061-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee061-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee061-138">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee061-138">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ee061-139">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee061-139">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ee061-140">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee061-140">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="ee061-141">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee061-141">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


