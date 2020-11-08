---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186591"
---
# <span data-ttu-id="789c9-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="789c9-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="789c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="789c9-102">SYNOPSIS</span></span>
<span data-ttu-id="789c9-103">Létrehoz egy olyan objektumot, amely az Azure-tárterület elérési útját jelöli egy webalkalmazásban való csatlakoztatáshoz.</span><span class="sxs-lookup"><span data-stu-id="789c9-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="789c9-104">A program paraméterként (-AzureStoragePath) használja Set-AzWebApp és Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="789c9-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="789c9-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="789c9-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="789c9-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="789c9-106">DESCRIPTION</span></span>
<span data-ttu-id="789c9-107">Létrehoz egy olyan objektumot, amely egy, az Azure tárolási útját jelképezi, és egy webalkalmazásban van elhelyezve.</span><span class="sxs-lookup"><span data-stu-id="789c9-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="789c9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="789c9-108">EXAMPLES</span></span>

### <span data-ttu-id="789c9-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="789c9-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="789c9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="789c9-110">PARAMETERS</span></span>

### <span data-ttu-id="789c9-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="789c9-111">-AccessKey</span></span>
<span data-ttu-id="789c9-112">Access-kulcs az Azure Storage-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="789c9-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="789c9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="789c9-113">-AccountName</span></span>
<span data-ttu-id="789c9-114">Azure Storage-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="789c9-114">Azure Storage account name.</span></span>
<span data-ttu-id="789c9-115">Például: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="789c9-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="789c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789c9-116">-DefaultProfile</span></span>
<span data-ttu-id="789c9-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="789c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="789c9-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="789c9-118">-MountPath</span></span>
<span data-ttu-id="789c9-119">Annak a tárolónak az elérési útja, ahol a megosztásnév által megadott megosztás ki lesz téve</span><span class="sxs-lookup"><span data-stu-id="789c9-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="789c9-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="789c9-120">-Name</span></span>
<span data-ttu-id="789c9-121">Az Azure Storage tulajdonság azonosítója.</span><span class="sxs-lookup"><span data-stu-id="789c9-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="789c9-122">Egyedinek kell lennie a Web App vagy a bővítőhelyen belül</span><span class="sxs-lookup"><span data-stu-id="789c9-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="789c9-123">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="789c9-123">-ShareName</span></span>
<span data-ttu-id="789c9-124">Annak a megosztásnak a neve, amelyet a tárolóhoz kell csatlakoztatni</span><span class="sxs-lookup"><span data-stu-id="789c9-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="789c9-125">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="789c9-125">-Type</span></span>
<span data-ttu-id="789c9-126">Az Azure Storage-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="789c9-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="789c9-127">A Windows-tárolók csak az Azure-fájlokat támogatják</span><span class="sxs-lookup"><span data-stu-id="789c9-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="789c9-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="789c9-128">-Confirm</span></span>
<span data-ttu-id="789c9-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="789c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789c9-130">-WhatIf</span></span>
<span data-ttu-id="789c9-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="789c9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="789c9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="789c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789c9-133">CommonParameters</span></span>
<span data-ttu-id="789c9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="789c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789c9-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789c9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789c9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="789c9-136">INPUTS</span></span>

### <span data-ttu-id="789c9-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="789c9-137">None</span></span>

## <span data-ttu-id="789c9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="789c9-138">OUTPUTS</span></span>

### <span data-ttu-id="789c9-139">Microsoft. Azure. Command. WebApps. models. WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="789c9-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="789c9-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="789c9-140">NOTES</span></span>

## <span data-ttu-id="789c9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="789c9-141">RELATED LINKS</span></span>
