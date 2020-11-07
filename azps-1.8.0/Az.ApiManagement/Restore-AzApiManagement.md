---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: 2343a42f3978a2811b68b4dccd50acd5f9430282
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836932"
---
# <span data-ttu-id="41de8-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="41de8-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="41de8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41de8-102">SYNOPSIS</span></span>
<span data-ttu-id="41de8-103">Egy API-kezelési szolgáltatás visszaállítása a megadott Azure Storage blob-ról</span><span class="sxs-lookup"><span data-stu-id="41de8-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="41de8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41de8-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41de8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="41de8-105">DESCRIPTION</span></span>
<span data-ttu-id="41de8-106">A **Restore-AzApiManagement** PARANCSMAG egy API-kezelési szolgáltatást ad vissza a megadott biztonsági másolatból egy Azurestorage blobban.</span><span class="sxs-lookup"><span data-stu-id="41de8-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="41de8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="41de8-107">EXAMPLES</span></span>

### <span data-ttu-id="41de8-108">Példa 1: API-kezelési szolgáltatás visszaállítása</span><span class="sxs-lookup"><span data-stu-id="41de8-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="41de8-109">A parancs visszaállítja az API-kezelési szolgáltatást az Azure Storage blob szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="41de8-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="41de8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41de8-110">PARAMETERS</span></span>

### <span data-ttu-id="41de8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41de8-111">-DefaultProfile</span></span>
<span data-ttu-id="41de8-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41de8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41de8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41de8-113">-Name</span></span>
<span data-ttu-id="41de8-114">A biztonsági másolattal visszaállított API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41de8-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="41de8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41de8-115">-PassThru</span></span>
<span data-ttu-id="41de8-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="41de8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="41de8-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="41de8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41de8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41de8-118">-ResourceGroupName</span></span>
<span data-ttu-id="41de8-119">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="41de8-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="41de8-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="41de8-120">-SourceBlobName</span></span>
<span data-ttu-id="41de8-121">Itt adhatja meg az Azure-tárterület biztonságimásolat-forrás blobjának a nevét.</span><span class="sxs-lookup"><span data-stu-id="41de8-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="41de8-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="41de8-122">-SourceContainerName</span></span>
<span data-ttu-id="41de8-123">Az Azure Storage Backup Source tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41de8-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="41de8-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="41de8-124">-StorageContext</span></span>
<span data-ttu-id="41de8-125">A tárterület-kapcsolat kontextusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="41de8-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="41de8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41de8-126">CommonParameters</span></span>
<span data-ttu-id="41de8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41de8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41de8-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41de8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41de8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41de8-129">INPUTS</span></span>

### <span data-ttu-id="41de8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="41de8-130">System.String</span></span>

## <span data-ttu-id="41de8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41de8-131">OUTPUTS</span></span>

### <span data-ttu-id="41de8-132">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="41de8-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="41de8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41de8-133">NOTES</span></span>

## <span data-ttu-id="41de8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41de8-134">RELATED LINKS</span></span>

[<span data-ttu-id="41de8-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="41de8-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="41de8-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="41de8-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="41de8-137">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="41de8-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="41de8-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="41de8-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


