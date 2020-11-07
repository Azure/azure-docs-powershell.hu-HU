---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f89d47dac0b48ca82b2478743d2993f94fb792d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835898"
---
# <span data-ttu-id="857e1-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="857e1-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="857e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="857e1-102">SYNOPSIS</span></span>
<span data-ttu-id="857e1-103">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="857e1-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="857e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="857e1-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="857e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="857e1-105">DESCRIPTION</span></span>
<span data-ttu-id="857e1-106">Megkapja a IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="857e1-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="857e1-107">A connectionStrings lekérheti az összes billentyűt, vagy szűrheti őket egy adott kulcs nevével.</span><span class="sxs-lookup"><span data-stu-id="857e1-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="857e1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="857e1-108">EXAMPLES</span></span>

### <span data-ttu-id="857e1-109">Példa 1 az összes IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="857e1-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="857e1-110">A "myiothub" nevű iothub tartozó összes kulcs connectionStrings kapja.</span><span class="sxs-lookup"><span data-stu-id="857e1-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="857e1-111">Példa 2 a IotHub connectionStrings beolvasása adott kulcshoz</span><span class="sxs-lookup"><span data-stu-id="857e1-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="857e1-112">A "Mykey" nevű kulcs connectionStrings kapja az "myiothub" nevű iothub</span><span class="sxs-lookup"><span data-stu-id="857e1-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="857e1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="857e1-113">PARAMETERS</span></span>

### <span data-ttu-id="857e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857e1-114">-DefaultProfile</span></span>
<span data-ttu-id="857e1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="857e1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="857e1-116">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="857e1-116">-KeyName</span></span>
<span data-ttu-id="857e1-117">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="857e1-117">Name of the Key</span></span>

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

### <span data-ttu-id="857e1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="857e1-118">-Name</span></span>
<span data-ttu-id="857e1-119">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="857e1-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="857e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="857e1-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="857e1-121">Resource Group Name</span></span>

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

### <span data-ttu-id="857e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857e1-122">CommonParameters</span></span>
<span data-ttu-id="857e1-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="857e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857e1-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="857e1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857e1-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="857e1-125">INPUTS</span></span>

### <span data-ttu-id="857e1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="857e1-126">System.String</span></span>

## <span data-ttu-id="857e1-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="857e1-127">OUTPUTS</span></span>

### <span data-ttu-id="857e1-128">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="857e1-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="857e1-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="857e1-129">NOTES</span></span>

## <span data-ttu-id="857e1-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="857e1-130">RELATED LINKS</span></span>
