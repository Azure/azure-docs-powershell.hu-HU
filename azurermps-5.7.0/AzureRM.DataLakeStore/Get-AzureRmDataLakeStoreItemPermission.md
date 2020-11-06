---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: f76473239661b492c95a356dfb1b381e1093f98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494510"
---
# <span data-ttu-id="9d7d0-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="9d7d0-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="9d7d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7d0-103">Az adattó-tárolóban lévő fájl vagy mappa engedélyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d7d0-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d7d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d7d0-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d7d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d7d0-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7d0-106">A **Get-AzureRmDataLakeStoreItemPermission** parancsmag az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét kapja.</span><span class="sxs-lookup"><span data-stu-id="9d7d0-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9d7d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d7d0-107">EXAMPLES</span></span>

### <span data-ttu-id="9d7d0-108">1. példa: a fájlhoz tartozó engedélyek beállítása</span><span class="sxs-lookup"><span data-stu-id="9d7d0-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="9d7d0-109">Ez a parancs beilleszti a fájlhoz tartozó engedély oktálisát.</span><span class="sxs-lookup"><span data-stu-id="9d7d0-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="9d7d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d7d0-110">PARAMETERS</span></span>

### <span data-ttu-id="9d7d0-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9d7d0-111">-Account</span></span>
<span data-ttu-id="9d7d0-112">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d7d0-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7d0-113">-DefaultProfile</span></span>
<span data-ttu-id="9d7d0-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d7d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7d0-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9d7d0-115">-Path</span></span>
<span data-ttu-id="9d7d0-116">A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="9d7d0-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7d0-117">CommonParameters</span></span>
<span data-ttu-id="9d7d0-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d7d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7d0-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7d0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7d0-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d7d0-120">INPUTS</span></span>

### <span data-ttu-id="9d7d0-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="9d7d0-121">None</span></span>
<span data-ttu-id="9d7d0-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9d7d0-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d7d0-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d7d0-123">OUTPUTS</span></span>

### <span data-ttu-id="9d7d0-124">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="9d7d0-124">string</span></span>
<span data-ttu-id="9d7d0-125">Az oktális tulajdonos karakterlánc-ábrázolása</span><span class="sxs-lookup"><span data-stu-id="9d7d0-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="9d7d0-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d7d0-126">NOTES</span></span>
* <span data-ttu-id="9d7d0-127">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="9d7d0-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="9d7d0-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d7d0-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d7d0-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="9d7d0-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


