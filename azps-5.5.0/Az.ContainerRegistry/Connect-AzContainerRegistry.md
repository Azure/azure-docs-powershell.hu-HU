---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 3c702d0572bb8e5bdf41deff599b9da6c5cc2dcf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209895"
---
# <span data-ttu-id="53169-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="53169-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="53169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53169-102">SYNOPSIS</span></span>
<span data-ttu-id="53169-103">Jelentkezzen be egy Azure Container beállításjegyzékbe.</span><span class="sxs-lookup"><span data-stu-id="53169-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="53169-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53169-104">SYNTAX</span></span>

### <span data-ttu-id="53169-105">WithoutNameAndPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53169-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53169-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="53169-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53169-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53169-107">DESCRIPTION</span></span>
<span data-ttu-id="53169-108">Jelentkezzen be egy Azure Container beállításjegyzékbe.</span><span class="sxs-lookup"><span data-stu-id="53169-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="53169-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53169-109">EXAMPLES</span></span>

### <span data-ttu-id="53169-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="53169-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="53169-111">Jelentkezzen be hitelesítő adatok nélkül az ACR szolgáltatásba, amikor már bejelentkezik az Azure-fiókba.</span><span class="sxs-lookup"><span data-stu-id="53169-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="53169-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="53169-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="53169-113">Jelentkezzen be az ACR szolgáltatásba rendszergazdai felhasználónévvel/jelszóval, ha a rendszergazdai felhasználó engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="53169-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="53169-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="53169-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="53169-115">Jelentkezzen be az ACR szolgáltatásba egyszerű alkalmazásazonosítóval és jelszóval.</span><span class="sxs-lookup"><span data-stu-id="53169-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="53169-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53169-116">PARAMETERS</span></span>

### <span data-ttu-id="53169-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53169-117">-DefaultProfile</span></span>
<span data-ttu-id="53169-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53169-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53169-119">-Name</span><span class="sxs-lookup"><span data-stu-id="53169-119">-Name</span></span>
<span data-ttu-id="53169-120">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="53169-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53169-121">-Password</span><span class="sxs-lookup"><span data-stu-id="53169-121">-Password</span></span>
<span data-ttu-id="53169-122">Az Azure Container Registry jelszava.</span><span class="sxs-lookup"><span data-stu-id="53169-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="53169-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="53169-123">-UserName</span></span>
<span data-ttu-id="53169-124">Az Azure Container Registry felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="53169-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="53169-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53169-125">CommonParameters</span></span>
<span data-ttu-id="53169-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53169-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53169-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53169-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53169-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53169-128">INPUTS</span></span>

### <span data-ttu-id="53169-129">System.String</span><span class="sxs-lookup"><span data-stu-id="53169-129">System.String</span></span>

## <span data-ttu-id="53169-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53169-130">OUTPUTS</span></span>

### <span data-ttu-id="53169-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="53169-131">System.Boolean</span></span>

## <span data-ttu-id="53169-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53169-132">NOTES</span></span>

## <span data-ttu-id="53169-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53169-133">RELATED LINKS</span></span>
