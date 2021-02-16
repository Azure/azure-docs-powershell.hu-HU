---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144323"
---
# <span data-ttu-id="14421-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="14421-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="14421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14421-102">SYNOPSIS</span></span>
<span data-ttu-id="14421-103">A Data Lake Store-ban tárolt fájl vagy mappa oktális engedélyét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="14421-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14421-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="14421-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14421-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="14421-105">DESCRIPTION</span></span>
<span data-ttu-id="14421-106">A **Get-AzDataLakeStoreItemPermission** parancsmag megkapja egy fájl vagy mappa oktális engedélyét a Data Lake Store-ban.</span><span class="sxs-lookup"><span data-stu-id="14421-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14421-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="14421-107">EXAMPLES</span></span>

### <span data-ttu-id="14421-108">1. példa: A fájl engedélyeinek oktális beállítása</span><span class="sxs-lookup"><span data-stu-id="14421-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="14421-109">Ez a parancs a fájl oktális engedélyét kapja.</span><span class="sxs-lookup"><span data-stu-id="14421-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="14421-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14421-110">PARAMETERS</span></span>

### <span data-ttu-id="14421-111">-Account</span><span class="sxs-lookup"><span data-stu-id="14421-111">-Account</span></span>
<span data-ttu-id="14421-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14421-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14421-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14421-113">-DefaultProfile</span></span>
<span data-ttu-id="14421-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="14421-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14421-115">-Path</span><span class="sxs-lookup"><span data-stu-id="14421-115">-Path</span></span>
<span data-ttu-id="14421-116">A fájl vagy mappa Data Lake Store-beli elérési útját adja meg a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="14421-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14421-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14421-117">CommonParameters</span></span>
<span data-ttu-id="14421-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14421-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14421-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14421-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14421-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14421-120">INPUTS</span></span>

### <span data-ttu-id="14421-121">System.String</span><span class="sxs-lookup"><span data-stu-id="14421-121">System.String</span></span>

### <span data-ttu-id="14421-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="14421-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="14421-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14421-123">OUTPUTS</span></span>

### <span data-ttu-id="14421-124">System.String</span><span class="sxs-lookup"><span data-stu-id="14421-124">System.String</span></span>

## <span data-ttu-id="14421-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="14421-125">NOTES</span></span>
* <span data-ttu-id="14421-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="14421-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="14421-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14421-127">RELATED LINKS</span></span>

[<span data-ttu-id="14421-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="14421-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


