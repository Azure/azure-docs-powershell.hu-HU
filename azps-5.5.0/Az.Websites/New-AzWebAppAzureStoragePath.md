---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149683"
---
# <span data-ttu-id="e26f0-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="e26f0-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="e26f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e26f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e26f0-103">Olyan objektumot hoz létre, amely egy Web Appban felvehető Azure Storage elérési utat képvisel.</span><span class="sxs-lookup"><span data-stu-id="e26f0-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="e26f0-104">Paraméterként (-AzureStoragePath) való használatra szolgál a Set-AzWebApp és Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e26f0-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="e26f0-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e26f0-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e26f0-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e26f0-106">DESCRIPTION</span></span>
<span data-ttu-id="e26f0-107">Olyan objektumot hoz létre, amely egy Azure Storage elérési utat képvisel, amely egy webalkalmazásba való felhelyzhető.</span><span class="sxs-lookup"><span data-stu-id="e26f0-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="e26f0-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e26f0-108">EXAMPLES</span></span>

### <span data-ttu-id="e26f0-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="e26f0-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="e26f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e26f0-110">PARAMETERS</span></span>

### <span data-ttu-id="e26f0-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="e26f0-111">-AccessKey</span></span>
<span data-ttu-id="e26f0-112">Az Azure Storage-fiók hozzáférési kulcsa</span><span class="sxs-lookup"><span data-stu-id="e26f0-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="e26f0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e26f0-113">-AccountName</span></span>
<span data-ttu-id="e26f0-114">Azure Storage-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e26f0-114">Azure Storage account name.</span></span>
<span data-ttu-id="e26f0-115">Például: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="e26f0-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="e26f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26f0-116">-DefaultProfile</span></span>
<span data-ttu-id="e26f0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e26f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e26f0-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="e26f0-118">-MountPath</span></span>
<span data-ttu-id="e26f0-119">Path in the container where the share specified by ShareName will be exposed</span><span class="sxs-lookup"><span data-stu-id="e26f0-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="e26f0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e26f0-120">-Name</span></span>
<span data-ttu-id="e26f0-121">Az Azure Storage tulajdonság azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e26f0-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="e26f0-122">Egyedinek kell lennie a webalkalmazáson vagy a sloton belül</span><span class="sxs-lookup"><span data-stu-id="e26f0-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="e26f0-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e26f0-123">-ShareName</span></span>
<span data-ttu-id="e26f0-124">A tárolóhoz csatlakoztatni megfelelő megosztás neve</span><span class="sxs-lookup"><span data-stu-id="e26f0-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="e26f0-125">-Type</span><span class="sxs-lookup"><span data-stu-id="e26f0-125">-Type</span></span>
<span data-ttu-id="e26f0-126">Az Azure Storage-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="e26f0-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="e26f0-127">A Windows-tárolók csak az Azure-fájlokat támogatják</span><span class="sxs-lookup"><span data-stu-id="e26f0-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26f0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e26f0-128">-Confirm</span></span>
<span data-ttu-id="e26f0-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e26f0-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26f0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e26f0-130">-WhatIf</span></span>
<span data-ttu-id="e26f0-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e26f0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e26f0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e26f0-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e26f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26f0-133">CommonParameters</span></span>
<span data-ttu-id="e26f0-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26f0-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e26f0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26f0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e26f0-136">INPUTS</span></span>

### <span data-ttu-id="e26f0-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="e26f0-137">None</span></span>

## <span data-ttu-id="e26f0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e26f0-138">OUTPUTS</span></span>

### <span data-ttu-id="e26f0-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="e26f0-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="e26f0-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e26f0-140">NOTES</span></span>

## <span data-ttu-id="e26f0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e26f0-141">RELATED LINKS</span></span>
