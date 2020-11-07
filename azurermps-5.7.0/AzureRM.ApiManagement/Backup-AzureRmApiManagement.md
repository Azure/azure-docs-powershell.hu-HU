---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: 0fd004cdb727a0e665fd9b867854b3b8e4054c9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680842"
---
# <span data-ttu-id="1640a-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1640a-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="1640a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1640a-102">SYNOPSIS</span></span>
<span data-ttu-id="1640a-103">Biztonsági másolatot készíthet egy API-kezelési szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="1640a-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1640a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1640a-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1640a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1640a-105">DESCRIPTION</span></span>
<span data-ttu-id="1640a-106">A **Backup-AzureRmApiManagement** parancsmag egy Azure API-kezelési szolgáltatás példányát támogatja.</span><span class="sxs-lookup"><span data-stu-id="1640a-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="1640a-107">Ez a parancsmag az Azure Storage blob néven tárolja a biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="1640a-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="1640a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1640a-108">EXAMPLES</span></span>

### <span data-ttu-id="1640a-109">1. példa: API-kezelési szolgáltatás biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="1640a-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="1640a-110">Ezzel a paranccsal biztonsági másolatot készíthet egy API-kezelési szolgáltatásról a tárolási blobra.</span><span class="sxs-lookup"><span data-stu-id="1640a-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="1640a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1640a-111">PARAMETERS</span></span>

### <span data-ttu-id="1640a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1640a-112">-DefaultProfile</span></span>
<span data-ttu-id="1640a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1640a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1640a-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1640a-114">-Name</span></span>
<span data-ttu-id="1640a-115">Itt adhatja meg az API-kezelés telepített példányának a nevét, amelyre a parancsmag biztonsági másolat készül.</span><span class="sxs-lookup"><span data-stu-id="1640a-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1640a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1640a-116">-PassThru</span></span>
<span data-ttu-id="1640a-117">Azt jelzi, hogy ez a parancsmag a biztonsági másolat **PsApiManagement** objektumát adja vissza, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="1640a-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1640a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1640a-118">-ResourceGroupName</span></span>
<span data-ttu-id="1640a-119">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="1640a-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1640a-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="1640a-120">-StorageContext</span></span>
<span data-ttu-id="1640a-121">A tárterület-kapcsolat kontextusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1640a-121">Specifies a storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1640a-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="1640a-122">-TargetBlobName</span></span>
<span data-ttu-id="1640a-123">A biztonsági másolat blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1640a-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="1640a-124">Ha a blob nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1640a-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="1640a-125">Ez a parancsmag a következő minta alapján hoz létre alapértelmezett értéket:</span><span class="sxs-lookup"><span data-stu-id="1640a-125">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="1640a-126">{Name}-{ÉÉÉÉ-HH-NN-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="1640a-126">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1640a-127">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="1640a-127">-TargetContainerName</span></span>
<span data-ttu-id="1640a-128">A biztonsági másolat blob-tárolójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1640a-128">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="1640a-129">Ha a tároló nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1640a-129">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="1640a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1640a-130">CommonParameters</span></span>
<span data-ttu-id="1640a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1640a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1640a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1640a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1640a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1640a-133">INPUTS</span></span>

### <span data-ttu-id="1640a-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="1640a-134">None</span></span>
<span data-ttu-id="1640a-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1640a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1640a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1640a-136">OUTPUTS</span></span>

### <span data-ttu-id="1640a-137">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1640a-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1640a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1640a-138">NOTES</span></span>

## <span data-ttu-id="1640a-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1640a-139">RELATED LINKS</span></span>

[<span data-ttu-id="1640a-140">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1640a-140">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="1640a-141">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1640a-141">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="1640a-142">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1640a-142">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="1640a-143">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1640a-143">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


