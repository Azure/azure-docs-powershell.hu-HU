---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672076"
---
# <span data-ttu-id="ef790-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef790-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="ef790-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef790-102">SYNOPSIS</span></span>
<span data-ttu-id="ef790-103">Egy API-kezelési szolgáltatás visszaállítása a megadott Azure Storage blob-ról</span><span class="sxs-lookup"><span data-stu-id="ef790-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef790-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef790-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef790-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef790-105">DESCRIPTION</span></span>
<span data-ttu-id="ef790-106">A **Restore-AzureRmApiManagement** PARANCSMAG egy API-kezelési szolgáltatást ad vissza a megadott biztonsági másolatból egy Azurestorage blobban.</span><span class="sxs-lookup"><span data-stu-id="ef790-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="ef790-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef790-107">EXAMPLES</span></span>

### <span data-ttu-id="ef790-108">Példa 1: API-kezelési szolgáltatás visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ef790-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="ef790-109">A parancs visszaállítja az API-kezelési szolgáltatást az Azure Storage blob szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="ef790-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="ef790-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef790-110">PARAMETERS</span></span>

### <span data-ttu-id="ef790-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef790-111">-Name</span></span>
<span data-ttu-id="ef790-112">A biztonsági másolattal visszaállított API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef790-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="ef790-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef790-113">-PassThru</span></span>
<span data-ttu-id="ef790-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ef790-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef790-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ef790-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef790-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef790-116">-ResourceGroupName</span></span>
<span data-ttu-id="ef790-117">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="ef790-117">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="ef790-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="ef790-118">-SourceBlobName</span></span>
<span data-ttu-id="ef790-119">Itt adhatja meg az Azure-tárterület biztonságimásolat-forrás blobjának a nevét.</span><span class="sxs-lookup"><span data-stu-id="ef790-119">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="ef790-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="ef790-120">-SourceContainerName</span></span>
<span data-ttu-id="ef790-121">Az Azure Storage Backup Source tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef790-121">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="ef790-122">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ef790-122">-StorageContext</span></span>
<span data-ttu-id="ef790-123">A tárterület-kapcsolat kontextusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef790-123">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef790-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef790-124">-DefaultProfile</span></span>
<span data-ttu-id="ef790-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef790-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef790-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef790-126">CommonParameters</span></span>
<span data-ttu-id="ef790-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef790-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef790-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef790-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef790-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef790-129">INPUTS</span></span>

## <span data-ttu-id="ef790-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef790-130">OUTPUTS</span></span>

### <span data-ttu-id="ef790-131">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef790-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ef790-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef790-132">NOTES</span></span>

## <span data-ttu-id="ef790-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef790-133">RELATED LINKS</span></span>

[<span data-ttu-id="ef790-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef790-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="ef790-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef790-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ef790-136">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef790-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ef790-137">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef790-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


