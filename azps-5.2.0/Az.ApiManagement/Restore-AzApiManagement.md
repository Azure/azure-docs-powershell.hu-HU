---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362583"
---
# <span data-ttu-id="9a5e8-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5e8-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="9a5e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5e8-103">Visszaállít egy API-kezelési szolgáltatást a megadott Azure-tárterület blobból.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="9a5e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a5e8-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a5e8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a5e8-105">DESCRIPTION</span></span>
<span data-ttu-id="9a5e8-106">A **Restore-AzApiManagement** parancsmag visszaállítja az API-felügyeleti szolgáltatást egy Azurestorage-blob adott biztonsági mentési környezetében.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="9a5e8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a5e8-107">EXAMPLES</span></span>

### <span data-ttu-id="9a5e8-108">1. példa: API-kezelési szolgáltatás visszaállítása</span><span class="sxs-lookup"><span data-stu-id="9a5e8-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="9a5e8-109">Ez a parancs visszaállít egy API-kezelési szolgáltatást az Azure storage blobból.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="9a5e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a5e8-110">PARAMETERS</span></span>

### <span data-ttu-id="9a5e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5e8-111">-DefaultProfile</span></span>
<span data-ttu-id="9a5e8-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a5e8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9a5e8-113">-Name</span></span>
<span data-ttu-id="9a5e8-114">Annak az API-kezelési példánynak a nevét adja meg, amely a biztonsági másolatsal együtt visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="9a5e8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a5e8-115">-PassThru</span></span>
<span data-ttu-id="9a5e8-116">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a5e8-117">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a5e8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5e8-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a5e8-119">Annak az erőforráscsoportnak a neve, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="9a5e8-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="9a5e8-120">-SourceBlobName</span></span>
<span data-ttu-id="9a5e8-121">Az Azure-tár biztonságimásolat-forrás blobja nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="9a5e8-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="9a5e8-122">-SourceContainerName</span></span>
<span data-ttu-id="9a5e8-123">Az Azure tár biztonságimásolat-tárolója nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="9a5e8-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="9a5e8-124">-StorageContext</span></span>
<span data-ttu-id="9a5e8-125">A tárterület-kapcsolat környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="9a5e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5e8-126">CommonParameters</span></span>
<span data-ttu-id="9a5e8-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5e8-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a5e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5e8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a5e8-129">INPUTS</span></span>

### <span data-ttu-id="9a5e8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9a5e8-130">System.String</span></span>

## <span data-ttu-id="9a5e8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a5e8-131">OUTPUTS</span></span>

### <span data-ttu-id="9a5e8-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5e8-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9a5e8-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a5e8-133">NOTES</span></span>

## <span data-ttu-id="9a5e8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a5e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a5e8-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5e8-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="9a5e8-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5e8-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="9a5e8-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5e8-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="9a5e8-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5e8-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


