---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501896"
---
# <span data-ttu-id="5415d-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5415d-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="5415d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5415d-102">SYNOPSIS</span></span>
<span data-ttu-id="5415d-103">Az adattó-tárolóban lévő fájl vagy mappa engedélyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5415d-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5415d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5415d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5415d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5415d-105">DESCRIPTION</span></span>
<span data-ttu-id="5415d-106">A **Get-AzureRmDataLakeStoreItemPermission** parancsmag az adattó-tárolóban lévő fájlok vagy mappák engedélyének oktális részét kapja.</span><span class="sxs-lookup"><span data-stu-id="5415d-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5415d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5415d-107">EXAMPLES</span></span>

### <span data-ttu-id="5415d-108">1. példa: a fájlhoz tartozó engedélyek beállítása</span><span class="sxs-lookup"><span data-stu-id="5415d-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="5415d-109">Ez a parancs beilleszti a fájlhoz tartozó engedély oktálisát.</span><span class="sxs-lookup"><span data-stu-id="5415d-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="5415d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5415d-110">PARAMETERS</span></span>

### <span data-ttu-id="5415d-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="5415d-111">-Account</span></span>
<span data-ttu-id="5415d-112">Az adattó áruházbeli fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5415d-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="5415d-113">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="5415d-113">-Path</span></span>
<span data-ttu-id="5415d-114">A fájl vagy mappa adattó-tároló elérési útját adja meg, a legfelső szintű könyvtárral (/) kezdve.</span><span class="sxs-lookup"><span data-stu-id="5415d-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5415d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5415d-115">-DefaultProfile</span></span>
<span data-ttu-id="5415d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5415d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5415d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5415d-117">CommonParameters</span></span>
<span data-ttu-id="5415d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5415d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5415d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5415d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5415d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5415d-120">INPUTS</span></span>

## <span data-ttu-id="5415d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5415d-121">OUTPUTS</span></span>

### <span data-ttu-id="5415d-122">karakterlánc</span><span class="sxs-lookup"><span data-stu-id="5415d-122">string</span></span>
<span data-ttu-id="5415d-123">Az oktális tulajdonos karakterlánc-ábrázolása</span><span class="sxs-lookup"><span data-stu-id="5415d-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="5415d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5415d-124">NOTES</span></span>
* <span data-ttu-id="5415d-125">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5415d-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="5415d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5415d-126">RELATED LINKS</span></span>

[<span data-ttu-id="5415d-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5415d-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


