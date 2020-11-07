---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666841"
---
# <span data-ttu-id="68fc0-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="68fc0-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="68fc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="68fc0-103">Az adattó-tárolóban lévő fájl vagy mappa engedélyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68fc0-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="68fc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68fc0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68fc0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="68fc0-106">A **Get-AzDataLakeStoreItemPermission** parancsmag az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét kapja.</span><span class="sxs-lookup"><span data-stu-id="68fc0-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="68fc0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68fc0-107">EXAMPLES</span></span>

### <span data-ttu-id="68fc0-108">1. példa: a fájlhoz tartozó engedélyek beállítása</span><span class="sxs-lookup"><span data-stu-id="68fc0-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="68fc0-109">Ez a parancs beilleszti a fájlhoz tartozó engedély oktálisát.</span><span class="sxs-lookup"><span data-stu-id="68fc0-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="68fc0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68fc0-110">PARAMETERS</span></span>

### <span data-ttu-id="68fc0-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="68fc0-111">-Account</span></span>
<span data-ttu-id="68fc0-112">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68fc0-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="68fc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fc0-113">-DefaultProfile</span></span>
<span data-ttu-id="68fc0-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68fc0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68fc0-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="68fc0-115">-Path</span></span>
<span data-ttu-id="68fc0-116">A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="68fc0-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="68fc0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fc0-117">CommonParameters</span></span>
<span data-ttu-id="68fc0-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68fc0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fc0-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fc0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fc0-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68fc0-120">INPUTS</span></span>

### <span data-ttu-id="68fc0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="68fc0-121">System.String</span></span>

### <span data-ttu-id="68fc0-122">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="68fc0-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="68fc0-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68fc0-123">OUTPUTS</span></span>

### <span data-ttu-id="68fc0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="68fc0-124">System.String</span></span>

## <span data-ttu-id="68fc0-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68fc0-125">NOTES</span></span>
* <span data-ttu-id="68fc0-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="68fc0-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="68fc0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68fc0-127">RELATED LINKS</span></span>

[<span data-ttu-id="68fc0-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="68fc0-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


