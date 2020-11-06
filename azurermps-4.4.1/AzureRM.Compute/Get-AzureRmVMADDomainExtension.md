---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e4431b657c72a82f1316f5eb8b74f45fac0f04aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493844"
---
# <span data-ttu-id="4e36c-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4e36c-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="4e36c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e36c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e36c-103">Információt AD a tartomány kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="4e36c-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e36c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e36c-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e36c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e36c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e36c-106">A **Get-AzureRmVMADDomainExtension** parancsmag információkat kap a megadott Azure Active Directory-tartomány (ad) tartomány-kiterjesztéséről.</span><span class="sxs-lookup"><span data-stu-id="4e36c-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="4e36c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4e36c-107">EXAMPLES</span></span>

## <span data-ttu-id="4e36c-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e36c-108">PARAMETERS</span></span>

### <span data-ttu-id="4e36c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e36c-109">-DefaultProfile</span></span>
<span data-ttu-id="4e36c-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e36c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e36c-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e36c-111">-Name</span></span>
<span data-ttu-id="4e36c-112">A tartomány kiterjesztésének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e36c-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e36c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e36c-113">-ResourceGroupName</span></span>
<span data-ttu-id="4e36c-114">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e36c-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4e36c-115">-Állapot</span><span class="sxs-lookup"><span data-stu-id="4e36c-115">-Status</span></span>
<span data-ttu-id="4e36c-116">Azt jelzi, hogy ez a parancsmag a tartományi bővítmény példány nézetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4e36c-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e36c-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="4e36c-117">-VMName</span></span>
<span data-ttu-id="4e36c-118">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e36c-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e36c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e36c-119">CommonParameters</span></span>
<span data-ttu-id="4e36c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e36c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e36c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e36c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e36c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e36c-122">INPUTS</span></span>

## <span data-ttu-id="4e36c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e36c-123">OUTPUTS</span></span>

## <span data-ttu-id="4e36c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e36c-124">NOTES</span></span>

## <span data-ttu-id="4e36c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e36c-125">RELATED LINKS</span></span>

[<span data-ttu-id="4e36c-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4e36c-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


