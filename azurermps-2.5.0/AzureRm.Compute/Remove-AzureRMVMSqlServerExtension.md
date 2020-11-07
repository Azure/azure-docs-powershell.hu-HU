---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850094"
---
# <span data-ttu-id="16113-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="16113-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="16113-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16113-102">SYNOPSIS</span></span>
<span data-ttu-id="16113-103">SQL Server-bővítmény eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="16113-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16113-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16113-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16113-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16113-105">DESCRIPTION</span></span>
<span data-ttu-id="16113-106">A **Remove-AzureRmVMSqlServerExtension** parancsmag eltávolítja a AzureSQL Server-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="16113-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="16113-107">Példák</span><span class="sxs-lookup"><span data-stu-id="16113-107">EXAMPLES</span></span>

### <span data-ttu-id="16113-108">1. példa: SQL Server-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="16113-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="16113-109">Ez a parancs eltávolítja az SQL Server-bővítményt a ContosoVM22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="16113-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="16113-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16113-110">PARAMETERS</span></span>

### <span data-ttu-id="16113-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16113-111">-DefaultProfile</span></span>
<span data-ttu-id="16113-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16113-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16113-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="16113-113">-Name</span></span>
<span data-ttu-id="16113-114">Annak az SQL-kiszolgálónak a neve, amely a parancsmag által eltávolított bővítmény.</span><span class="sxs-lookup"><span data-stu-id="16113-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16113-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16113-115">-ResourceGroupName</span></span>
<span data-ttu-id="16113-116">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="16113-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16113-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="16113-117">-VMName</span></span>
<span data-ttu-id="16113-118">Annak a virtuális gépnek a neve, amelyből a parancsmag eltávolítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="16113-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16113-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16113-119">CommonParameters</span></span>
<span data-ttu-id="16113-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16113-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16113-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16113-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16113-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16113-122">INPUTS</span></span>

### <span data-ttu-id="16113-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="16113-123">None</span></span>
<span data-ttu-id="16113-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="16113-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16113-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16113-125">OUTPUTS</span></span>

### <span data-ttu-id="16113-126">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="16113-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="16113-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16113-127">NOTES</span></span>

## <span data-ttu-id="16113-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16113-128">RELATED LINKS</span></span>

[<span data-ttu-id="16113-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="16113-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="16113-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="16113-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


