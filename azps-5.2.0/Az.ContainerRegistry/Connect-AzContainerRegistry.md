---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344681"
---
# <span data-ttu-id="6c971-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6c971-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="6c971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c971-102">SYNOPSIS</span></span>
<span data-ttu-id="6c971-103">Jelentkezzen be egy Azure Container beállításjegyzékbe.</span><span class="sxs-lookup"><span data-stu-id="6c971-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="6c971-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c971-104">SYNTAX</span></span>

### <span data-ttu-id="6c971-105">WithoutNameAndPasswordParameterSet (default)</span><span class="sxs-lookup"><span data-stu-id="6c971-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c971-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c971-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c971-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c971-107">DESCRIPTION</span></span>
<span data-ttu-id="6c971-108">Jelentkezzen be egy Azure Container beállításjegyzékbe.</span><span class="sxs-lookup"><span data-stu-id="6c971-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="6c971-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c971-109">EXAMPLES</span></span>

### <span data-ttu-id="6c971-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="6c971-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="6c971-111">Jelentkezzen be hitelesítő adatokkal az ACR szolgáltatásba, amikor már bejelentkezik az Azure-fiókba.</span><span class="sxs-lookup"><span data-stu-id="6c971-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="6c971-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="6c971-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="6c971-113">Jelentkezzen be az ACR szolgáltatásba rendszergazdai felhasználónévvel/jelszóval, ha a rendszergazdai felhasználó engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="6c971-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="6c971-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="6c971-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="6c971-115">Jelentkezzen be az ACR szolgáltatásba egyszerű alkalmazásazonosítóval és jelszóval.</span><span class="sxs-lookup"><span data-stu-id="6c971-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="6c971-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c971-116">PARAMETERS</span></span>

### <span data-ttu-id="6c971-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c971-117">-DefaultProfile</span></span>
<span data-ttu-id="6c971-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c971-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c971-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6c971-119">-Name</span></span>
<span data-ttu-id="6c971-120">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="6c971-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c971-121">-Password</span><span class="sxs-lookup"><span data-stu-id="6c971-121">-Password</span></span>
<span data-ttu-id="6c971-122">Az Azure Container Registry jelszava.</span><span class="sxs-lookup"><span data-stu-id="6c971-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c971-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="6c971-123">-UserName</span></span>
<span data-ttu-id="6c971-124">Az Azure Container Registry felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="6c971-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c971-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c971-125">CommonParameters</span></span>
<span data-ttu-id="6c971-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c971-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c971-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c971-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c971-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c971-128">INPUTS</span></span>

### <span data-ttu-id="6c971-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6c971-129">System.String</span></span>

## <span data-ttu-id="6c971-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c971-130">OUTPUTS</span></span>

### <span data-ttu-id="6c971-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c971-131">System.Boolean</span></span>

## <span data-ttu-id="6c971-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c971-132">NOTES</span></span>

## <span data-ttu-id="6c971-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c971-133">RELATED LINKS</span></span>
