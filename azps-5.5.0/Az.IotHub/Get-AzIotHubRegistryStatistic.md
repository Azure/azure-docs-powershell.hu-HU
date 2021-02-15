---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152874"
---
# <span data-ttu-id="24daa-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="24daa-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="24daa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24daa-102">SYNOPSIS</span></span>
<span data-ttu-id="24daa-103">Az IotHub Beállításjegyzék-statisztikáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24daa-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="24daa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="24daa-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24daa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="24daa-105">DESCRIPTION</span></span>
<span data-ttu-id="24daa-106">Az IotHub Beállításjegyzék-statisztikáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24daa-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="24daa-107">Ez a témakör az IotHub eszközön található összes, engedélyezett és letiltott eszköz számára vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="24daa-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="24daa-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="24daa-108">EXAMPLES</span></span>

### <span data-ttu-id="24daa-109">1. példa a Beállításstatisztika lekérte</span><span class="sxs-lookup"><span data-stu-id="24daa-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="24daa-110">A "myiothub" nevű IotHub beállításjegyzékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24daa-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="24daa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24daa-111">PARAMETERS</span></span>

### <span data-ttu-id="24daa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24daa-112">-DefaultProfile</span></span>
<span data-ttu-id="24daa-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="24daa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24daa-114">-Name</span><span class="sxs-lookup"><span data-stu-id="24daa-114">-Name</span></span>
<span data-ttu-id="24daa-115">Az IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="24daa-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="24daa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24daa-116">-ResourceGroupName</span></span>
<span data-ttu-id="24daa-117">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="24daa-117">Resource Group Name</span></span>

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

### <span data-ttu-id="24daa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24daa-118">CommonParameters</span></span>
<span data-ttu-id="24daa-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24daa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24daa-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24daa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24daa-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24daa-121">INPUTS</span></span>

### <span data-ttu-id="24daa-122">System.String</span><span class="sxs-lookup"><span data-stu-id="24daa-122">System.String</span></span>

## <span data-ttu-id="24daa-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24daa-123">OUTPUTS</span></span>

### <span data-ttu-id="24daa-124">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="24daa-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="24daa-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="24daa-125">NOTES</span></span>

## <span data-ttu-id="24daa-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24daa-126">RELATED LINKS</span></span>
