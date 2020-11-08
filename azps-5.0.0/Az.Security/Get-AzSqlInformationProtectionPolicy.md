---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186197"
---
# <span data-ttu-id="714e7-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="714e7-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="714e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="714e7-102">SYNOPSIS</span></span>
<span data-ttu-id="714e7-103">Visszanyeri a tényleges bérlői SQL-adatvédelemi házirendet.</span><span class="sxs-lookup"><span data-stu-id="714e7-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="714e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="714e7-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="714e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="714e7-105">DESCRIPTION</span></span>
<span data-ttu-id="714e7-106">Visszanyeri a tényleges bérlői SQL-adatvédelemi házirendet.</span><span class="sxs-lookup"><span data-stu-id="714e7-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="714e7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="714e7-107">EXAMPLES</span></span>

### <span data-ttu-id="714e7-108">Például</span><span class="sxs-lookup"><span data-stu-id="714e7-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="714e7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="714e7-109">PARAMETERS</span></span>

### <span data-ttu-id="714e7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="714e7-110">-AsJob</span></span>
<span data-ttu-id="714e7-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="714e7-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="714e7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714e7-112">-DefaultProfile</span></span>
<span data-ttu-id="714e7-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="714e7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="714e7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714e7-114">CommonParameters</span></span>
<span data-ttu-id="714e7-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="714e7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714e7-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="714e7-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714e7-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="714e7-117">INPUTS</span></span>

### <span data-ttu-id="714e7-118">System. String</span><span class="sxs-lookup"><span data-stu-id="714e7-118">System.string</span></span>

## <span data-ttu-id="714e7-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="714e7-119">OUTPUTS</span></span>

### <span data-ttu-id="714e7-120">Microsoft. Azure. Command. SecurityCenter. models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="714e7-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="714e7-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="714e7-121">NOTES</span></span>

## <span data-ttu-id="714e7-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="714e7-122">RELATED LINKS</span></span>
