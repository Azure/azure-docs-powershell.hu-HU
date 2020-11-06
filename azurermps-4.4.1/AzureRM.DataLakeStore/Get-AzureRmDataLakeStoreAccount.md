---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493516"
---
# <span data-ttu-id="22d1a-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22d1a-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="22d1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="22d1a-103">Adatokat kap az adattó áruházbeli fiókról.</span><span class="sxs-lookup"><span data-stu-id="22d1a-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22d1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22d1a-104">SYNTAX</span></span>

### <span data-ttu-id="22d1a-105">All in előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22d1a-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d1a-106">Minden az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="22d1a-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22d1a-107">Konkrét fiók</span><span class="sxs-lookup"><span data-stu-id="22d1a-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22d1a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="22d1a-108">DESCRIPTION</span></span>
<span data-ttu-id="22d1a-109">A **Get-AzureRmDataLakeStoreAccount** parancsmag az adattó-tároló fiók adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="22d1a-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="22d1a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="22d1a-110">EXAMPLES</span></span>

### <span data-ttu-id="22d1a-111">Példa 1: adattó áruházbeli fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="22d1a-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="22d1a-112">Ez a parancs a ContosoADL nevű fiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="22d1a-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="22d1a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22d1a-113">PARAMETERS</span></span>

### <span data-ttu-id="22d1a-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22d1a-114">-Name</span></span>
<span data-ttu-id="22d1a-115">A beolvasott fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d1a-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d1a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d1a-116">-ResourceGroupName</span></span>
<span data-ttu-id="22d1a-117">Az adattó-tároló fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d1a-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d1a-118">-DefaultProfile</span></span>
<span data-ttu-id="22d1a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22d1a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22d1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d1a-120">CommonParameters</span></span>
<span data-ttu-id="22d1a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22d1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d1a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d1a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d1a-123">INPUTS</span></span>

## <span data-ttu-id="22d1a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d1a-124">OUTPUTS</span></span>

### <span data-ttu-id="22d1a-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22d1a-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="22d1a-126">A meghatározott Data Lake Store-fiók.</span><span class="sxs-lookup"><span data-stu-id="22d1a-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="22d1a-127">Lista<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="22d1a-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="22d1a-128">Az adattó-tároló fiókjainak listája az erőforrás csoportban vagy az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="22d1a-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="22d1a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22d1a-129">NOTES</span></span>

## <span data-ttu-id="22d1a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22d1a-130">RELATED LINKS</span></span>

[<span data-ttu-id="22d1a-131">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22d1a-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="22d1a-132">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22d1a-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="22d1a-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22d1a-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="22d1a-134">Teszt-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="22d1a-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


