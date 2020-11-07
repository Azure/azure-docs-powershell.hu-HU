---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 3de18d5d7cc1c3525f1526beb5dd7337175eb041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680833"
---
# <span data-ttu-id="ee27c-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee27c-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="ee27c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee27c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee27c-103">Egy API-kezelési szolgáltatás visszaállítása a megadott Azure Storage blob-ról</span><span class="sxs-lookup"><span data-stu-id="ee27c-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee27c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee27c-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee27c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee27c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee27c-106">A **Restore-AzureRmApiManagement** PARANCSMAG egy API-kezelési szolgáltatást ad vissza a megadott biztonsági másolatból egy Azurestorage blobban.</span><span class="sxs-lookup"><span data-stu-id="ee27c-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="ee27c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee27c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee27c-108">Példa 1: API-kezelési szolgáltatás visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ee27c-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="ee27c-109">A parancs visszaállítja az API-kezelési szolgáltatást az Azure Storage blob szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="ee27c-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="ee27c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee27c-110">PARAMETERS</span></span>

### <span data-ttu-id="ee27c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee27c-111">-DefaultProfile</span></span>
<span data-ttu-id="ee27c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee27c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ee27c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee27c-113">-Name</span></span>
<span data-ttu-id="ee27c-114">A biztonsági másolattal visszaállított API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee27c-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="ee27c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee27c-115">-PassThru</span></span>
<span data-ttu-id="ee27c-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ee27c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee27c-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ee27c-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee27c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee27c-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee27c-119">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="ee27c-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="ee27c-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="ee27c-120">-SourceBlobName</span></span>
<span data-ttu-id="ee27c-121">Itt adhatja meg az Azure-tárterület biztonságimásolat-forrás blobjának a nevét.</span><span class="sxs-lookup"><span data-stu-id="ee27c-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="ee27c-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="ee27c-122">-SourceContainerName</span></span>
<span data-ttu-id="ee27c-123">Az Azure Storage Backup Source tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee27c-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="ee27c-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ee27c-124">-StorageContext</span></span>
<span data-ttu-id="ee27c-125">A tárterület-kapcsolat kontextusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee27c-125">Specifies the storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee27c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee27c-126">CommonParameters</span></span>
<span data-ttu-id="ee27c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee27c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee27c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee27c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee27c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee27c-129">INPUTS</span></span>

### <span data-ttu-id="ee27c-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee27c-130">None</span></span>
<span data-ttu-id="ee27c-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ee27c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee27c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee27c-132">OUTPUTS</span></span>

### <span data-ttu-id="ee27c-133">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee27c-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ee27c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee27c-134">NOTES</span></span>

## <span data-ttu-id="ee27c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee27c-135">RELATED LINKS</span></span>

[<span data-ttu-id="ee27c-136">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee27c-136">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="ee27c-137">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee27c-137">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ee27c-138">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee27c-138">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ee27c-139">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ee27c-139">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


