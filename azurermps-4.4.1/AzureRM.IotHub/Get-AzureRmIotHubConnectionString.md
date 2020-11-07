---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: 52c5bee4e699ff063794f140ce4360669180a164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679437"
---
# <span data-ttu-id="d7c2a-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="d7c2a-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="d7c2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c2a-103">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="d7c2a-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7c2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7c2a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7c2a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c2a-106">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="d7c2a-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="d7c2a-107">A connectionStrings lekérheti az összes billentyűt, vagy szűrheti őket egy adott kulcs nevével.</span><span class="sxs-lookup"><span data-stu-id="d7c2a-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="d7c2a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d7c2a-108">EXAMPLES</span></span>

### <span data-ttu-id="d7c2a-109">Példa 1 az összes IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="d7c2a-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d7c2a-110">A "myiothub" nevű iothub tartozó összes kulcs connectionStrings kapja.</span><span class="sxs-lookup"><span data-stu-id="d7c2a-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="d7c2a-111">Példa 2 a IotHub connectionStrings beolvasása adott kulcshoz</span><span class="sxs-lookup"><span data-stu-id="d7c2a-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="d7c2a-112">A "Mykey" nevű kulcs connectionStrings kapja az "myiothub" nevű iothub</span><span class="sxs-lookup"><span data-stu-id="d7c2a-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="d7c2a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7c2a-113">PARAMETERS</span></span>

### <span data-ttu-id="d7c2a-114">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="d7c2a-114">-KeyName</span></span>
<span data-ttu-id="d7c2a-115">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="d7c2a-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c2a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7c2a-116">-Name</span></span>
<span data-ttu-id="d7c2a-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="d7c2a-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c2a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c2a-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7c2a-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d7c2a-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c2a-120">-DefaultProfile</span></span>
<span data-ttu-id="d7c2a-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7c2a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7c2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c2a-122">CommonParameters</span></span>
<span data-ttu-id="d7c2a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7c2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c2a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c2a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c2a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7c2a-125">INPUTS</span></span>

### <span data-ttu-id="d7c2a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d7c2a-126">System.String</span></span>

## <span data-ttu-id="d7c2a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7c2a-127">OUTPUTS</span></span>

### <span data-ttu-id="d7c2a-128">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d7c2a-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="d7c2a-129">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="d7c2a-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="d7c2a-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7c2a-130">NOTES</span></span>

## <span data-ttu-id="d7c2a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7c2a-131">RELATED LINKS</span></span>

