---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: c4f5fe5fa703d2706d37cd0bebf9df79fd272f5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002902"
---
# <span data-ttu-id="591b4-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="591b4-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="591b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591b4-102">SYNOPSIS</span></span>
<span data-ttu-id="591b4-103">Tároló blobtárolók lekérte vagy listázza a tárolókat</span><span class="sxs-lookup"><span data-stu-id="591b4-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="591b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="591b4-104">SYNTAX</span></span>

### <span data-ttu-id="591b4-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="591b4-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591b4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="591b4-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="591b4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="591b4-107">DESCRIPTION</span></span>
<span data-ttu-id="591b4-108">A **Get-AzRmStorageContainer** parancsmag lekérte vagy felsorolja a tároló blobtárolóit</span><span class="sxs-lookup"><span data-stu-id="591b4-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="591b4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="591b4-109">EXAMPLES</span></span>

### <span data-ttu-id="591b4-110">1. példa: Tárterület blobtárolója tárfiók nevével és tárolónevével</span><span class="sxs-lookup"><span data-stu-id="591b4-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="591b4-111">Ez a parancs egy Tároló blobtárolót kap, amely tárfióknevet és tárolónevet is ad.</span><span class="sxs-lookup"><span data-stu-id="591b4-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="591b4-112">2. példa: Tárfiók összes tárterület blobtárolója</span><span class="sxs-lookup"><span data-stu-id="591b4-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="591b4-113">Ez a parancs felsorolja egy Tárfiók tárfiók nevét tartalmazó tárterület blobtárolóját.</span><span class="sxs-lookup"><span data-stu-id="591b4-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="591b4-114">3. példa: Tárterület blobtárolója tárfiók-objektummal és tárolónévvel.</span><span class="sxs-lookup"><span data-stu-id="591b4-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="591b4-115">Ez a parancs egy Tároló blobtárolót kap a Tárfiók-objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="591b4-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="591b4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="591b4-116">PARAMETERS</span></span>

### <span data-ttu-id="591b4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="591b4-117">-AsJob</span></span>
<span data-ttu-id="591b4-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="591b4-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="591b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591b4-119">-DefaultProfile</span></span>
<span data-ttu-id="591b4-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="591b4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="591b4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="591b4-121">-Name</span></span>
<span data-ttu-id="591b4-122">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="591b4-122">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="591b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="591b4-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="591b4-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591b4-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="591b4-125">-StorageAccount</span></span>
<span data-ttu-id="591b4-126">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="591b4-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="591b4-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="591b4-127">-StorageAccountName</span></span>
<span data-ttu-id="591b4-128">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="591b4-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591b4-129">CommonParameters</span></span>
<span data-ttu-id="591b4-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591b4-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591b4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591b4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="591b4-132">INPUTS</span></span>

### <span data-ttu-id="591b4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="591b4-133">System.String</span></span>

### <span data-ttu-id="591b4-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="591b4-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="591b4-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="591b4-135">OUTPUTS</span></span>

### <span data-ttu-id="591b4-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="591b4-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="591b4-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="591b4-137">NOTES</span></span>

## <span data-ttu-id="591b4-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="591b4-138">RELATED LINKS</span></span>
