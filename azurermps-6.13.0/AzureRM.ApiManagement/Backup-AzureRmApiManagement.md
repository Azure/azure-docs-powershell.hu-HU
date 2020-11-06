---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d8f243b0b02d724a3979b8c8f318be8e58623cf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501259"
---
# <span data-ttu-id="e10be-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e10be-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="e10be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e10be-102">SYNOPSIS</span></span>
<span data-ttu-id="e10be-103">Biztonsági másolatot készíthet egy API-kezelési szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="e10be-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e10be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e10be-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e10be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e10be-105">DESCRIPTION</span></span>
<span data-ttu-id="e10be-106">A **Backup-AzureRmApiManagement** parancsmag egy Azure API-kezelési szolgáltatás példányát támogatja.</span><span class="sxs-lookup"><span data-stu-id="e10be-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="e10be-107">Ez a parancsmag az Azure Storage blob néven tárolja a biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="e10be-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="e10be-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e10be-108">EXAMPLES</span></span>

### <span data-ttu-id="e10be-109">1. példa: API-kezelési szolgáltatás biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="e10be-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="e10be-110">Ezzel a paranccsal biztonsági másolatot készíthet egy API-kezelési szolgáltatásról a tárolási blobra.</span><span class="sxs-lookup"><span data-stu-id="e10be-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="e10be-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e10be-111">PARAMETERS</span></span>

### <span data-ttu-id="e10be-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10be-112">-DefaultProfile</span></span>
<span data-ttu-id="e10be-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e10be-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e10be-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e10be-114">-Name</span></span>
<span data-ttu-id="e10be-115">Itt adhatja meg az API-kezelés telepített példányának a nevét, amelyre a parancsmag biztonsági másolat készül.</span><span class="sxs-lookup"><span data-stu-id="e10be-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="e10be-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e10be-116">-PassThru</span></span>
<span data-ttu-id="e10be-117">Azt jelzi, hogy ez a parancsmag a biztonsági másolat **PsApiManagement** objektumát adja vissza, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="e10be-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="e10be-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10be-118">-ResourceGroupName</span></span>
<span data-ttu-id="e10be-119">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="e10be-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="e10be-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e10be-120">-StorageContext</span></span>
<span data-ttu-id="e10be-121">A tárterület-kapcsolat kontextusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e10be-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="e10be-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="e10be-122">-TargetBlobName</span></span>
<span data-ttu-id="e10be-123">A biztonsági másolat blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e10be-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="e10be-124">Ha a blob nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e10be-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="e10be-125">Ez a parancsmag alapértelmezett értéket hoz létre a következő minta alapján: {Name}-{yyyy-HH-NN-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="e10be-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="e10be-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="e10be-126">-TargetContainerName</span></span>
<span data-ttu-id="e10be-127">A biztonsági másolat blob-tárolójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e10be-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="e10be-128">Ha a tároló nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e10be-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="e10be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10be-129">CommonParameters</span></span>
<span data-ttu-id="e10be-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e10be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10be-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e10be-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10be-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e10be-132">INPUTS</span></span>

### <span data-ttu-id="e10be-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e10be-133">System.String</span></span>

### <span data-ttu-id="e10be-134">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e10be-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e10be-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e10be-135">OUTPUTS</span></span>

### <span data-ttu-id="e10be-136">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e10be-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e10be-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e10be-137">NOTES</span></span>

## <span data-ttu-id="e10be-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e10be-138">RELATED LINKS</span></span>

[<span data-ttu-id="e10be-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e10be-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="e10be-140">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e10be-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="e10be-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e10be-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="e10be-142">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e10be-142">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


