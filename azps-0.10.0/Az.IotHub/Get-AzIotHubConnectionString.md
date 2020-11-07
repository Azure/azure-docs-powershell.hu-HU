---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: 92d1e3f2ef1ba87a5e9683f7ac6617e31bb8a055
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842242"
---
# <span data-ttu-id="af946-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="af946-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="af946-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af946-102">SYNOPSIS</span></span>
<span data-ttu-id="af946-103">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="af946-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="af946-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af946-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af946-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af946-105">DESCRIPTION</span></span>
<span data-ttu-id="af946-106">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="af946-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="af946-107">A connectionStrings lekérheti az összes billentyűt, vagy szűrheti őket egy adott kulcs nevével.</span><span class="sxs-lookup"><span data-stu-id="af946-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="af946-108">Példák</span><span class="sxs-lookup"><span data-stu-id="af946-108">EXAMPLES</span></span>

### <span data-ttu-id="af946-109">Példa 1 az összes IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="af946-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="af946-110">A "myiothub" nevű iothub tartozó összes kulcs connectionStrings kapja.</span><span class="sxs-lookup"><span data-stu-id="af946-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="af946-111">Példa 2 a IotHub connectionStrings beolvasása adott kulcshoz</span><span class="sxs-lookup"><span data-stu-id="af946-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="af946-112">A "Mykey" nevű kulcs connectionStrings kapja az "myiothub" nevű iothub</span><span class="sxs-lookup"><span data-stu-id="af946-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="af946-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af946-113">PARAMETERS</span></span>

### <span data-ttu-id="af946-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af946-114">-DefaultProfile</span></span>
<span data-ttu-id="af946-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="af946-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af946-116">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="af946-116">-KeyName</span></span>
<span data-ttu-id="af946-117">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="af946-117">Name of the Key</span></span>

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

### <span data-ttu-id="af946-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af946-118">-Name</span></span>
<span data-ttu-id="af946-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="af946-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="af946-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af946-120">-ResourceGroupName</span></span>
<span data-ttu-id="af946-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="af946-121">Resource Group Name</span></span>

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

### <span data-ttu-id="af946-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af946-122">CommonParameters</span></span>
<span data-ttu-id="af946-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af946-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af946-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af946-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af946-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af946-125">INPUTS</span></span>

### <span data-ttu-id="af946-126">System. String</span><span class="sxs-lookup"><span data-stu-id="af946-126">System.String</span></span>

## <span data-ttu-id="af946-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af946-127">OUTPUTS</span></span>

### <span data-ttu-id="af946-128">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="af946-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="af946-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af946-129">NOTES</span></span>

## <span data-ttu-id="af946-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af946-130">RELATED LINKS</span></span>
