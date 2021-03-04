---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 1f0ceb4f349e7fdfee38837561dc436c16cd451b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939034"
---
# <span data-ttu-id="c2027-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2027-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="c2027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2027-102">SYNOPSIS</span></span>
<span data-ttu-id="c2027-103">Api-kezelő szolgáltatás biztonsági biztonsági szolgáltatása.</span><span class="sxs-lookup"><span data-stu-id="c2027-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="c2027-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2027-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2027-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2027-105">DESCRIPTION</span></span>
<span data-ttu-id="c2027-106">A **Backup-AzApiManagement** parancsmag biztonsági másolatot készít egy Azure API Felügyeleti szolgáltatás egy példányáról.</span><span class="sxs-lookup"><span data-stu-id="c2027-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="c2027-107">Ez a parancsmag Azure Storage blobként tárolja a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="c2027-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="c2027-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2027-108">EXAMPLES</span></span>

### <span data-ttu-id="c2027-109">1. példa: API-kezelési szolgáltatás biztonsági</span><span class="sxs-lookup"><span data-stu-id="c2027-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="c2027-110">Ez a parancs egy API-kezelési szolgáltatásról biztonsági biztonsági adatokat nyújt egy tár blobban.</span><span class="sxs-lookup"><span data-stu-id="c2027-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="c2027-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2027-111">PARAMETERS</span></span>

### <span data-ttu-id="c2027-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2027-112">-DefaultProfile</span></span>
<span data-ttu-id="c2027-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2027-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2027-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c2027-114">-Name</span></span>
<span data-ttu-id="c2027-115">Annak az API Management-telepítésnek a nevét adja meg, amelyről a parancsmag biztonsági adatokat biztonságiolt.</span><span class="sxs-lookup"><span data-stu-id="c2027-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="c2027-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2027-116">-PassThru</span></span>
<span data-ttu-id="c2027-117">Azt jelzi, hogy ez a parancsmag a **psapiManagement** objektumról biztonságiolt objektumot ad vissza, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="c2027-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="c2027-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2027-118">-ResourceGroupName</span></span>
<span data-ttu-id="c2027-119">Annak az erőforráscsoportnak a nevét adja meg, amely alatt az API-kezelési telepítés létezik.</span><span class="sxs-lookup"><span data-stu-id="c2027-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="c2027-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c2027-120">-StorageContext</span></span>
<span data-ttu-id="c2027-121">Tárterület-kapcsolat környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2027-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="c2027-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="c2027-122">-TargetBlobName</span></span>
<span data-ttu-id="c2027-123">A biztonsági másolat blobnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2027-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="c2027-124">Ha a blob nem létezik, ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c2027-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="c2027-125">Ez a parancsmag a következő minta alapján hoz létre alapértelmezett értéket: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span><span class="sxs-lookup"><span data-stu-id="c2027-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="c2027-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="c2027-126">-TargetContainerName</span></span>
<span data-ttu-id="c2027-127">A biztonsági másolat blobtárolóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2027-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="c2027-128">Ha a tároló nem létezik, ez a parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c2027-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="c2027-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2027-129">CommonParameters</span></span>
<span data-ttu-id="c2027-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2027-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2027-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2027-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2027-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2027-132">INPUTS</span></span>

### <span data-ttu-id="c2027-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c2027-133">System.String</span></span>

### <span data-ttu-id="c2027-134">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c2027-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2027-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2027-135">OUTPUTS</span></span>

### <span data-ttu-id="c2027-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2027-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c2027-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2027-137">NOTES</span></span>

## <span data-ttu-id="c2027-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2027-138">RELATED LINKS</span></span>

[<span data-ttu-id="c2027-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2027-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="c2027-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2027-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="c2027-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2027-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="c2027-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c2027-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


