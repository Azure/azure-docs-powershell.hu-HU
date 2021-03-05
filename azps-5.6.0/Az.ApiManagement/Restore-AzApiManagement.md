---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d1c7e1938d50e4a970dbec15568bc5cf10257639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007382"
---
# <span data-ttu-id="049fd-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="049fd-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="049fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="049fd-102">SYNOPSIS</span></span>
<span data-ttu-id="049fd-103">Visszaállít egy API-kezelési szolgáltatást a megadott Azure-tárterület blobból.</span><span class="sxs-lookup"><span data-stu-id="049fd-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="049fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="049fd-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="049fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="049fd-105">DESCRIPTION</span></span>
<span data-ttu-id="049fd-106">A **Restore-AzApiManagement** parancsmag visszaállítja az API-felügyeleti szolgáltatást egy Azurestorage-blob adott biztonsági mentési környezetében.</span><span class="sxs-lookup"><span data-stu-id="049fd-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="049fd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="049fd-107">EXAMPLES</span></span>

### <span data-ttu-id="049fd-108">1. példa: API-kezelési szolgáltatás visszaállítása</span><span class="sxs-lookup"><span data-stu-id="049fd-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="049fd-109">Ez a parancs visszaállít egy API-kezelési szolgáltatást az Azure storage blobból.</span><span class="sxs-lookup"><span data-stu-id="049fd-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="049fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="049fd-110">PARAMETERS</span></span>

### <span data-ttu-id="049fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049fd-111">-DefaultProfile</span></span>
<span data-ttu-id="049fd-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="049fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="049fd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="049fd-113">-Name</span></span>
<span data-ttu-id="049fd-114">Annak az API-kezelési példánynak a nevét adja meg, amely a biztonsági másolatsal együtt visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="049fd-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="049fd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="049fd-115">-PassThru</span></span>
<span data-ttu-id="049fd-116">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="049fd-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="049fd-117">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="049fd-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="049fd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="049fd-118">-ResourceGroupName</span></span>
<span data-ttu-id="049fd-119">Annak az erőforráscsoportnak a neve, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="049fd-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="049fd-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="049fd-120">-SourceBlobName</span></span>
<span data-ttu-id="049fd-121">Az Azure-tár biztonságimásolat-forrás blobja nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="049fd-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="049fd-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="049fd-122">-SourceContainerName</span></span>
<span data-ttu-id="049fd-123">Az Azure tár biztonságimásolat-tárolója nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="049fd-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="049fd-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="049fd-124">-StorageContext</span></span>
<span data-ttu-id="049fd-125">A tárterület-kapcsolat környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="049fd-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="049fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049fd-126">CommonParameters</span></span>
<span data-ttu-id="049fd-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049fd-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="049fd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049fd-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="049fd-129">INPUTS</span></span>

### <span data-ttu-id="049fd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="049fd-130">System.String</span></span>

## <span data-ttu-id="049fd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="049fd-131">OUTPUTS</span></span>

### <span data-ttu-id="049fd-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="049fd-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="049fd-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="049fd-133">NOTES</span></span>

## <span data-ttu-id="049fd-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="049fd-134">RELATED LINKS</span></span>

[<span data-ttu-id="049fd-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="049fd-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="049fd-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="049fd-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="049fd-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="049fd-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="049fd-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="049fd-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


