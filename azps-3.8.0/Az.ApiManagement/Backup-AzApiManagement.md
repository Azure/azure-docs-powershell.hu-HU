---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011962"
---
# <span data-ttu-id="2b714-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b714-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="2b714-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b714-102">SYNOPSIS</span></span>
<span data-ttu-id="2b714-103">Biztonsági másolatot készíthet egy API-kezelési szolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="2b714-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="2b714-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b714-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b714-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b714-105">DESCRIPTION</span></span>
<span data-ttu-id="2b714-106">A **Backup-AzApiManagement** parancsmag egy Azure API-kezelési szolgáltatás példányát támogatja.</span><span class="sxs-lookup"><span data-stu-id="2b714-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="2b714-107">Ez a parancsmag az Azure Storage blob néven tárolja a biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="2b714-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="2b714-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2b714-108">EXAMPLES</span></span>

### <span data-ttu-id="2b714-109">1. példa: API-kezelési szolgáltatás biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="2b714-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="2b714-110">Ezzel a paranccsal biztonsági másolatot készíthet egy API-kezelési szolgáltatásról a tárolási blobra.</span><span class="sxs-lookup"><span data-stu-id="2b714-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="2b714-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b714-111">PARAMETERS</span></span>

### <span data-ttu-id="2b714-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b714-112">-DefaultProfile</span></span>
<span data-ttu-id="2b714-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b714-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b714-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b714-114">-Name</span></span>
<span data-ttu-id="2b714-115">Itt adhatja meg az API-kezelés telepített példányának a nevét, amelyre a parancsmag biztonsági másolat készül.</span><span class="sxs-lookup"><span data-stu-id="2b714-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="2b714-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b714-116">-PassThru</span></span>
<span data-ttu-id="2b714-117">Azt jelzi, hogy ez a parancsmag a biztonsági másolat **PsApiManagement** objektumát adja vissza, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="2b714-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="2b714-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b714-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b714-119">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="2b714-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="2b714-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="2b714-120">-StorageContext</span></span>
<span data-ttu-id="2b714-121">A tárterület-kapcsolat kontextusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b714-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="2b714-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="2b714-122">-TargetBlobName</span></span>
<span data-ttu-id="2b714-123">A biztonsági másolat blobjának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b714-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="2b714-124">Ha a blob nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b714-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="2b714-125">Ez a parancsmag alapértelmezett értéket hoz létre a következő minta alapján: {Name}-{yyyy-HH-NN-HH-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="2b714-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="2b714-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="2b714-126">-TargetContainerName</span></span>
<span data-ttu-id="2b714-127">A biztonsági másolat blob-tárolójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b714-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="2b714-128">Ha a tároló nem létezik, akkor ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b714-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="2b714-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b714-129">CommonParameters</span></span>
<span data-ttu-id="2b714-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b714-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b714-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2b714-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b714-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b714-132">INPUTS</span></span>

### <span data-ttu-id="2b714-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2b714-133">System.String</span></span>

### <span data-ttu-id="2b714-134">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b714-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2b714-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b714-135">OUTPUTS</span></span>

### <span data-ttu-id="2b714-136">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b714-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2b714-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b714-137">NOTES</span></span>

## <span data-ttu-id="2b714-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b714-138">RELATED LINKS</span></span>

[<span data-ttu-id="2b714-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b714-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="2b714-140">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b714-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="2b714-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b714-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="2b714-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b714-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


