---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187757"
---
# <span data-ttu-id="0f928-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f928-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="0f928-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f928-102">SYNOPSIS</span></span>
<span data-ttu-id="0f928-103">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="0f928-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="0f928-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f928-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f928-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f928-105">DESCRIPTION</span></span>
<span data-ttu-id="0f928-106">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="0f928-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="0f928-107">A connectionStrings lekérheti az összes billentyűt, vagy szűrheti őket egy adott kulcs nevével.</span><span class="sxs-lookup"><span data-stu-id="0f928-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="0f928-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0f928-108">EXAMPLES</span></span>

### <span data-ttu-id="0f928-109">Példa 1 az összes IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="0f928-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0f928-110">A "myiothub" nevű iothub tartozó összes kulcs connectionStrings kapja.</span><span class="sxs-lookup"><span data-stu-id="0f928-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="0f928-111">Példa 2 a IotHub connectionStrings beolvasása adott kulcshoz</span><span class="sxs-lookup"><span data-stu-id="0f928-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="0f928-112">A "Mykey" nevű kulcs connectionStrings kapja az "myiothub" nevű iothub</span><span class="sxs-lookup"><span data-stu-id="0f928-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="0f928-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f928-113">PARAMETERS</span></span>

### <span data-ttu-id="0f928-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f928-114">-DefaultProfile</span></span>
<span data-ttu-id="0f928-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f928-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f928-116">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="0f928-116">-KeyName</span></span>
<span data-ttu-id="0f928-117">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="0f928-117">Name of the Key</span></span>

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

### <span data-ttu-id="0f928-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f928-118">-Name</span></span>
<span data-ttu-id="0f928-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="0f928-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="0f928-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f928-120">-ResourceGroupName</span></span>
<span data-ttu-id="0f928-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0f928-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0f928-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f928-122">CommonParameters</span></span>
<span data-ttu-id="0f928-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f928-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f928-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f928-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f928-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f928-125">INPUTS</span></span>

### <span data-ttu-id="0f928-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0f928-126">System.String</span></span>

## <span data-ttu-id="0f928-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f928-127">OUTPUTS</span></span>

### <span data-ttu-id="0f928-128">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0f928-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0f928-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f928-129">NOTES</span></span>

## <span data-ttu-id="0f928-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f928-130">RELATED LINKS</span></span>
